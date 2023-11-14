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
I have 1 year of experience, working on client-server desktop applications for Windows.
In 2021-2022 I attended .NET courses, where studied OOP and SOLID principles, Dependency Injection, Configuration and Logging in C#, asynchronous programming in C#, common C# interfaces, LINQ, testing with NUnit and MOQ, worked with ADO.NET, EF core, ASP.NET core frameworks.
*****
### Education:
*2019-2023*  
**COMPUTERS, SYSTEMS AND NETWORKS, BSUIR**  
*AVERAGE GRADE: 8.34/10*

*2021-2022*  
**.NET COURSES, EPAM**
*****
### English level:
* English - B2+; In 2022 i graduated a Streamline English course. Also, for a couple of years now, in my day-to-day life I prefer to turn to english media, articles, documentations, etc.
* Russian - native;
