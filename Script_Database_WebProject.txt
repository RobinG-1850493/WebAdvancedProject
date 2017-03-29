DROP DATABASE Project_web;
CREATE DATABASE Project_web;

USE Project_web;

CREATE TABLE klanten (
    id INT(5) NOT NULL AUTO_INCREMENT,
    v_naam VARCHAR(20) NOT NULL,
    a_naam VARCHAR(30) NOT NULL,
    email VARCHAR(50) NOT NULL,
    geb_jaar INT (4) NOT NULL,
    PRIMARY KEY(id)
);

CREATE TABLE events (
    id INT(5) NOT NULL AUTO_INCREMENT,
    k_id INT (5) NOT NULL,
    naam VARCHAR(50) NOT NULL,
    b_datum DATETIME NOT NULL,
    e_datum DATETIME NOT NULL,
    locatie VARCHAR(50) NOT NULL,
    PRIMARY KEY(id)
);

INSERT INTO klanten (v_naam, a_naam, email, geb_jaar) VALUES ('Jos', 'Dewilde', 'JosDewilde@email.com', 1990);
INSERT INTO klanten (v_naam, a_naam, email, geb_jaar) VALUES ('Roos', 'Vanateren', 'RoosVanateren@email.com', 1989);
INSERT INTO klanten (v_naam, a_naam, email, geb_jaar) VALUES ('Ben', 'Leant', 'BenLeant@email.com', 1901);
INSERT INTO klanten (v_naam, a_naam, email, geb_jaar) VALUES ('Lisa', 'Garis', 'LisaGaris@email.com', 1998);

INSERT INTO events (k_id, naam, b_datum, e_datum, locatie) VALUES (2, 'Verrassingsfuif', '2017-09-05 16:30:00', '2017-09-06 03:00:00', 'Kerkstraat 27 Hasselt');
INSERT INTO events (k_id, naam, b_datum, e_datum, locatie) VALUES (4, 'Begrafenis', '2017-05-10 18:00:00', '2017-05-10 22:00:00', 'Grafhoflaan 666 Zonhoven');
INSERT INTO events (k_id, naam, b_datum, e_datum, locatie) VALUES (1, 'Trouwfeest', '2020-01-02 12:15:00', '2020-01-02 20:30:00', 'Nieuwjaarsstraat 1 Bilzen');
INSERT INTO events (k_id, naam, b_datum, e_datum, locatie) VALUES (3, 'AA-bijeenkomst', '2030-06-09 14:45:45', '2030-06-09 15:30:30', 'Jeneverlaan 50 Hasselt');

SELECT * FROM klanten;
SELECT * FROM events;
 
