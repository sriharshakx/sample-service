import hudson.model.*
import hudson.maven.*
import hudson.tasks.*

for(item in Hudson.instance.items)
{
  println("job $item.name")
  item.setDescription("<img src='buildTimeGraph/png' />");
}

node() {

  buildName "NEW"
  buildDescription "NEW1 TO DESC\nNEW2\nNEW3\nVul\nN\na\nvb\nc"

  stage('Code Checkout') {
    echo 'Code Checkout'
  }
}

