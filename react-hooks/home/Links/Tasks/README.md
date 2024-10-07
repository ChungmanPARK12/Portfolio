```js
import React, {useState, useEffect} from 'react';
import uuid from 'uuid/v4';

const TASKS_STORAGE_KEY = 'TASKS_STORAGE_KEY';

const storeTasks = (taskMap) => {
    localStorage.setItem(
        TASKS_STORAGE_KEY,
        JSON.stringify(taskMap)
    );
}

const readStoredTasks = () => {
    const tasksMap = JSON.parse(localStorage.getItem(TASKS_STORAGE_KEY));

    return tasksMap ? tasksMap : {tasks: [], completedTasks: []}; 
}
// let i = 0;

function Tasks() {
    const [taskText, setTaskText] = useState('');
    const storedTasks = readStoredTasks();
    const [tasks, setTasks] = useState(storedTasks.tasks);
    const [completedTasks, setCompletedTasks] = useState(storedTasks.completedTasks);

    // let tasks, setTasks, completedTasks, setCompletedTasks;

    // if (i%2==0) {
    //   ([tasks, setTasks] = useState([storedTasks.tasks]));
    //   ([completedTasks, setCompletedTasks] = useState([storedTasks.completedTask]));
    // } else {
    //     ([completedTasks, setCompletedTasks] = useState([storedTasks.tasks]));
    //     ([tasks, setTasks] = useState([storedTasks.completedTask]));
    // }

    // i++;

    useEffect(() => {
        storeTasks({tasks, completedTasks});
    })

    const updateTaskText = event => {
        setTaskText(event.target.value);
    }

    const addTask = () => {
        setTasks([...tasks, {taskText, id: uuid()}]);
    }

    const completeTask = completedTask => () => {
        setCompletedTasks([...completedTasks, completedTask]);
        setTasks(tasks.filter(task => task.id !== completedTask.id));
    }

    const deleteTask = task => () => {
        setCompletedTasks(completedTasks.filter(t => t.id !== task.id));
    }

    return (
        <div>
            <h3>Tasks</h3>
            <div className='form'>
                <input value={taskText} onChange={updateTaskText}/>
                <button onClick={addTask}>Add Task</button>
            </div>
            <div className='task-list'>
                {
                    tasks.map(task => {
                        const {id, taskText} = task;
                        
                        return (
                           <div key={id} onClick={completeTask(task)}>{taskText}</div>
                        );
                    })
                }
            </div>
            <div className='completed-list'>
                {
                    completedTasks.map(task => {
                        const {id, taskText} = task;

                        return (
                            <div key={id}>
                              {taskText}{' '}
                              <span onClick={deleteTask(task)}className='delete-task'>x</span>
                             </div>
                        )
                    })
                }
            </div>
        </div>
    )
}
export default Tasks;
```