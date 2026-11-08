```sql
-- ==================================================
-- DATABASE: caio
-- PURPOSE: An attempt to document a human being.
-- STATUS: Under development.
-- ==================================================

CREATE DATABASE IF NOT EXISTS caio;

USE caio;


-- ------------------------------------------
-- 01. IDENTIFICATION
-- ------------------------------------------

CREATE TABLE identity (
    id          INTEGER PRIMARY KEY,
    name        VARCHAR(50),
    species     VARCHAR(50),
    occupation  VARCHAR(100),
    status      VARCHAR(50)
);

INSERT INTO identity (
    id, name, species, occupation, status
) VALUES (
    1,
    'Caio',
    'Human',
    'Computer Engineering Undergraduate',
    'Still figuring things out'
);


-- ------------------------------------------
-- 02. CURRENTLY EXPLORING
-- ------------------------------------------

CREATE TABLE ongoing_exploration (
    subject VARCHAR(100),
    status  VARCHAR(50)
);

INSERT INTO ongoing_exploration VALUES
    ('Embedded Systems', 'In progress'),
    ('Computer Architecture', 'In progress'),
    ('Firmware Development', 'In progress'),
    ('Low-Level Programming', 'In progress'),
    ('Software Engineering', 'In progress');


-- ------------------------------------------
-- 03. UNANSWERED QUESTIONS
-- ------------------------------------------

CREATE TABLE unanswered_questions (
    question TEXT,
    answer   TEXT DEFAULT NULL
);

INSERT INTO unanswered_questions (question) VALUES
    ('How does everything work?'),
    ('Why does everything work?'),
    ('What am I doing?');


-- ------------------------------------------
-- 04. QUERY EXECUTION
-- ------------------------------------------

SELECT * FROM identity;

SELECT * FROM ongoing_exploration;

SELECT question, answer
FROM unanswered_questions
WHERE answer IS NULL;


-- ==================================================
-- QUERY RESULTS:
--
-- Identity:       FOUND
-- Exploration:    ONGOING
-- Answers:        NOT FOUND
-- Existence:      CONFIRMED
--
-- ==================================================

-- The investigation continues...
```
