# Alexey Smolik
### Full-stack developer
### Contact Info:

```
email: smolikvtanke@gmail.com
skype: executer_1010
```

### Skills:
```
Programming languages: JavaScript, C++, C#, Node.JS, Angular, Angular 2+
Frameworks: Express.JS, sequelize
Methodologies: Scrum
Version control: github, gitlub
Data bases: PostgreSQL, MySQL, Oracle
Tools: Intellij IDEA, Web Storm, Visual Studio, Visual Studo Code
```
### Education:
```
BSTU 2014-2018
    Faculty of Information Technologies
    
Magistracy: 2018-current
```
### Code examples:
##### Node.JS:
```
// ----- ROUTES FOR ROOMS ISSUES -----
// --- GET ISSUES BY RoomId ---
routes.get('/:id/issues', (req, res) => {
    let where = req.query.active ? { roomId: req.params.id, active: req.query.active } : { roomId: req.params.id };
    issues.findAll({ where: where, order: [['id', 'DESC']], include: [{model: rooms, attributes : ['name']}] })
        .then(issues => {
            res.send(issues);
        })
        .catch(err => {
            res.status(500).send({message: err.message});
        });
});
```
##### Angular.JS:
```
$scope.getSelectedAreas = () => $scope.areas ? $scope.areas : "Please select an area";
$scope.getSelectedCountry = () => $scope.country ? $scope.country : "Please select a country";
```