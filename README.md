# React-Mini-Pro
# mini pro on inputs
# Box1.js:
```js
import React,{useState} from 'react';
function Box1()
{
   const [name,setname]=useState("");
   const [num,setNum]=useState(0);
   const [boolean,setBoolean]=useState(false);
   //List
   const [skills,setSkills]=useState([]);
   const [skill,setSkill]=useState("");
   const addSkill=()=>{
    if(skill==="")return;
    setSkills([...skills,skill]);
    setSkill("");
   }

   return(
    <div>
      <h1>Mini project1</h1>
      
      <input type="text" onChange={(e)=>setname(e.target.value)}></input>
    <p>Name:{name}</p>
    <input type="number" onChange={(e)=>setNum(e.target.value)}/>
    <p>Number:{num}</p>
    <input type="checkbox" onChange={(e)=>setBoolean(!boolean)}/>
    <p>{boolean?"student":"not student"}</p>
    <hr />
   <h2> List: adding skills:</h2>
   <input type="text" value={skill} onChange={(e)=>setSkill(e.target.value)} />
   <button onClick={addSkill}> Add Skill</button>
     <ul>
      {skills.map((s,index)=>
      (
        <li key={index}>{s}</li>

      ))
    }
</ul>
    </div>
   )
}
export default Box1;
```

