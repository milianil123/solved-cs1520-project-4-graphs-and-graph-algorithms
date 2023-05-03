Download Link: https://assignmentchef.com/product/solved-cs1520-project-4-graphs-and-graph-algorithms
<br>
To gain a better understanding of graphs and graph algorithms through practical implementation.

<h1>High-level description</h1>

Your program will analyze a given graph representing a computer network according to several specified metrics. The vertices of these graphs will represent switches in the network, while the edges represent either fiber optic or copper cables run between the switches. Your program should operate entirely via a console interface menu (no GUI).

<h1>Specifications</h1>

<ol>

 <li>Your program should accept a single command-line argument that specifies the name of a file containing the description of a graph. Two such files are provided, network_data1.txt and</li>

</ol>

network_data2.txt . The format of these files is as follows:

The first line contains a single int stating the number of vertices in the graph. These vertices will be numbered 0 to v-1.

Each subsequent line describes a single edge in the graph, with each of the following data items listed separated by spaces.

First, two integers specify the endpoints of the edge.

Next, a string describes the type of cable the edge represents (either “optical” or “copper”).

Next, an integer states the bandwidth of the cable in megabits per second.

Finally, an integer states the length of the edge in meters.

As an example, the line 0 5 optical 10000 25 describes an edge between vertex 0 and vertex 5 that represents a 25 meter optical cable with bandwidth of 10 gigabits per second.

Assume that all cables are full duplex and hence represent connections in both directions (e.g., in the example above, data can flow from vertex 0 to vertex 5 at 10 gigabits per second and from vertex 5 to vertex 0 at 10 gigabits per second simultaneously).

<ol start="2">

 <li>You must internally represent the graph as an adjacency list.</li>

 <li>After loading the graph from the specified file, your program should present the user with a menu with the following options:

  <ol>

   <li>Find the <strong>lowest latency path</strong> between any two points, and give the bandwidth available along that path.

    <ol>

     <li>First, your program should prompt the user for the two vertices between which they wish to find the lowest latency path.</li>

     <li>Then, your program should output the sequence of vertices that comprise the lowest-latency path, in order from the first user-specified vertex to the second.</li>

    </ol></li>

  </ol></li>

</ol>

You must find the path between these vertices that will require the least amount of time for a single data packet to travel. For this project, assume that the time required to travel along a path through the graph is the sum of the times required to travel each link, and that the time to travel each link is equal to the length of the cable divided by the speed at which data can be sent (determined by the link type).

Assume data can be sent along a copper cable at a speed of 230,000,000 meters per second.

Assume data can be sent along a fiber optic cable at a speed of 200,000,000 meters per second.

<ol start="3">

 <li>Finally, your program should output the bandwidth that is available along the resulting path (i.e., the minimum bandwidth of all the edges in the path).</li>

</ol>

<ol start="2">

 <li>Determine whether or not the graph is <strong>copper-only connected</strong>, or connected when considering only copper links (i.e., ignore fiber optic cables).</li>

 <li>Find the <strong>maximum amount of data</strong> that can be transmitted from one vertex to another.

  <ol>

   <li>First, your program should prompt the user for the two vertices between which they wish to find the bandwidth.</li>

   <li>Then, your program should output the maximum amount of data that can be transmitted from the first to second user-specified vertices.</li>

  </ol></li>

 <li>Find the <strong>minimum average latency spanning tree</strong> for the graph, the spanning tree with the lowest average latency per edge.</li>

 <li>Determine whether the graph would remain connected even if <strong>any two vertices fail</strong>.</li>

</ol>

<strong>Note:</strong> You are not prompting the user for two vertices that could fail, you need to determine whether there is <em>any pair</em> of vertices that, should they both fail, would cause the graph to become disconnected.

<ol start="6">

 <li>Quit the program.</li>

</ol>