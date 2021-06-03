# MonitorSensorProject
1. Собрать в Maven и задеплоить в Tomcat(Использовалась 8 версия)

2. В postgresql выполнить запросы
create database monitorsensorsdb;

create table sensor_units(unit_id bigint primary key, name varchar(10));

insert into sensor_units(unit_id, name) values (1, 'bar'), (2, 'voltage'), (3, 'C'), (4,'%');

create table sensor_types(type_id bigint primary key, name varchar(40));

insert into sensor_types(type_id, name) values (1,'Pressure'), (2,'Voltage'), (3, 'Temperature'), (4, 'Humidity');

CREATE TABLE sensors ( sensor_id bigint primary key,  name  varchar(30) not null, model varchar(15) not null, range_from int, range_to int, type_id bigint, unit_id bigint, location varchar(40), description varchar(200));

insert into sensors(sensor_id, name, model, type_id, range_from, range_to, unit_id, location, description) values (1, 'Sensor 1', 'PC33-56', 1, 0, 16, 1, 'Room1', 'Desription of Sensor 1'), (2, 'Sensor 2', 'EH-567', 2, -25, 25, 2, 'Room1', 'Description of Sensor 2'), (3, 'Sensor 3', 'TER-21', 3, -70, 50, 3, 'Room3', 'Decsription of Sensor 3'), (4, 'Sensor 4', 'H94', 4, 0, 100, 4, 'Room3', 'Desription of Sensor 4');

3. Запустить frontend.
