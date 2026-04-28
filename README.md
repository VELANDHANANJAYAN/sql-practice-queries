-- Create table
CREATE TABLE Candidates (
    id INT PRIMARY KEY,
    name VARCHAR(50),
    skills VARCHAR(100),
    experience INT,
    status VARCHAR(20)
);

-- Insert data
INSERT INTO Candidates VALUES
(1, 'Arun', 'Java, SQL', 2, 'Applied'),
(2, 'Priya', 'Python, ML', 3, 'Shortlisted'),
(3, 'Rahul', 'Java, Spring', 1, 'Rejected');

-- Basic query
SELECT * FROM Candidates;

-- Filter
SELECT name FROM Candidates WHERE experience > 2;

-- Aggregate
SELECT COUNT(*) FROM Candidates;

-- Join example
CREATE TABLE Jobs (
    job_id INT,
    role VARCHAR(50)
);

SELECT Candidates.name, Jobs.role
FROM Candidates
INNER JOIN Jobs ON Candidates.id = Jobs.job_id;
