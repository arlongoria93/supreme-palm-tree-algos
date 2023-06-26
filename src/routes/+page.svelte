<script>
  const row = document.querySelectorAll(".row");
  console.log(row);
  let twoDArray = [
    [1, 2, 3, 4],
    [5, 6, 7, 8],
    [9, 10, 11, 12],
    [13, 14, 15, 16],
  ];

  const dfs = (x, y, targetNode) => {
    const visited = new Set();
    const stack = [];
    stack.push([x, y]);

    while (stack.length >= 1) {
      const node = stack.pop();
      if (twoDArray[node[0]][node[1]] === targetNode) {
        console.log(node);

        return stack;
      }
      if (!visited.has(twoDArray[node[0]][node[1]])) {
        //get adjacents and add to stack
        addToStack(node, stack);
        visited.add(twoDArray[node[0]][node[1]]);
      }
    }

    console.log("not found");
  };

  //right y+1
  //left y-1
  //top x-1
  //bottom x+1

  const addToStack = (currentNode, stack) => {
    const [x, y] = currentNode;

    if (y < twoDArray[x].length - 1) {
      const right = [x, y + 1];
      stack.push(right);
    }

    if (x < twoDArray.length - 1) {
      const bottom = [x + 1, y];
      stack.push(bottom);
    }

    if (y - 1 >= 0) {
      const left = [x, y - 1];
      stack.push(left);
    }

    if (x - 1 >= 0) {
      const top = [x - 1, y];
      stack.push(top);
    }
  };

  dfs(1, 2, 17); //stack = [8,11,6,3]

  // add current node to the stack
  // add current node to the visited set
  // add adjacent nodes to the stack
</script>

<h1>Welcome to SvsdsdelteKit</h1>
<div class="container">
  <div class="row">
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
  </div>
  <div class="row">
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
  </div>
  <div class="row">
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
  </div>
  <div class="row">
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
  </div>
  <div class="row">
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
  </div>
  <div class="row">
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
  </div>
  <div class="row">
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
  </div>
  <div class="row">
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
  </div>
  <div class="row">
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
  </div>
  <div class="row">
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
    <div class="blox" />
  </div>
</div>

<style>
  .container {
    width: 100%;
    align-items: center;
    justify-content: center;
    display: flex;
    grid-template-columns: repeat(5, auto);
    padding: 10;
  }
  .blox {
    height: 50px;
    width: 50px;
    background-color: brown;
    border: 1px solid black;
  }
</style>
