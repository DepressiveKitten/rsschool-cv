# Dmitriy Lopatin
*****
### Contacts:
* **Mail**: mityalopatin12321@gmail.com 
* **Telegram**: [@PositiveKitten](https://t.me/PositiveKitten)
* **Github**: [DepressiveKitten](https://github.com/DepressiveKitten)
* **GitLab**: [mityalopatin12321](https://gitlab.com/mityalopatin12321)
*****
### About Me:
I am a fast learner and like picking up new skills in different fields. I take all the tasks responsibly and always try to meet my deadlines. Difficulties don’t scare me and I always try my best to find the best solution.
*****
### Skills:
* **C#**; Frameworks: ADO.NET, **EF core**, **ASP.NET** core, NUnit, WFP, WinForms
* **C++**; STL, boost, MPI
* Experience with **Git** and **TFS**
* **SQL** (postgresql, mssql, sqlite)
* Experience with **Bash**
* System programming
* Knowledge in computer networks
*****
### Code Example:
Code from [Design Graph With Shortest Path Calculator](https://leetcode.com/problems/design-graph-with-shortest-path-calculator/) task on [Leetcode](https://leetcode.com/mityalopatin12321/)
```
typedef pair<int, int> pi;
class Graph {
private:
    unordered_map<int, vector<pair<int, int>>> graph;
public:
    Graph(int n, const vector<vector<int>>& edges) {
        for (auto edge : edges)
        {
            graph[edge[0]].push_back(make_pair(edge[1], edge[2]));
        }
    }

    void addEdge(const vector<int> edge) {
        graph[edge[0]].push_back(make_pair(edge[1], edge[2]));
    }

    int shortestPath(int node1, int node2) {
        priority_queue<pi, vector<pi>, greater<pi> > weights;
        unordered_set<int> visited;
        unordered_map<int,int> optimization;

        weights.push(pair<int, int>(0, node1));
        while (!weights.empty())
        {
            int weight = weights.top().first;
            int node = weights.top().second;

            if (visited.count(node) == 1)
            {
                weights.pop();
                continue;
            }

            if (node == node2)
            {
                return weight;
            }

            visited.insert(node);
            weights.pop();

            for (auto graph_pair : graph[node])
            {
                if (visited.count(graph_pair.first) < 1&&(optimization.count(graph_pair.first)==0||optimization[graph_pair.first]>weight + graph_pair.second))
                {
                    weights.push(pair<int, int>(weight + graph_pair.second, graph_pair.first));
                    optimization[graph_pair.first]=weight + graph_pair.second;
                }
            }
        }
        return -1;
    }
};
```
*****
### Expirience:
*****
### Education:
*****
### English level:
