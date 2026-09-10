function dailyLog167() {
  const tasks = [
    { name: "Fix a bug", priority: 9 },
    { name: "Read documentation", priority: 6 },
    { name: "Write tests", priority: 8 },
    { name: "Update notes", priority: 4 },
    { name: "Review code", priority: 7 }
  ];

  const sortedTasks = [...tasks].sort(
    (a, b) => b.priority - a.priority
  );

  const report = {
    date: new Date().toISOString().split("T")[0],
    totalTasks: tasks.length,
    highestPriority: sortedTasks[0].name,
    priorityScore: sortedTasks[0].priority,
    taskOrder: sortedTasks.map(task => task.name)
  };

  console.log("Daily Priority Report:", report);
}

dailyLog167();
