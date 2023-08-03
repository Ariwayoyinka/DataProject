# DataProject
mysql -u root --local-infile=1 -p
show variables like "local_infile";
create database Marketdata;
use Marketdata;
create table Googledata(Marketday date, Open float, High float, Low float, Close float, AdjClose float, Volume float);
load data local infile "/Users/oluwatosinariwayo/Downloads/Googledata.csv" into table Googledata fields terminated by "," optionally enclosed by "'" ignore 1 lines;
select * from Googledata;
