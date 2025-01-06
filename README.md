# Neha-arch
Hello world this is my portfolio
import java.util.ArrayList;
import java.util.List;

public class Portfolio {

    // Personal Information
    private String name;
    private String email;
    private String phoneNumber;
    private String linkedin;
    private String github;

    // List of skills
    private List<String> skills;

    // List of projects
    private List<Project> projects;

    // Constructor to initialize personal details
    public Portfolio(String name, String email, String phoneNumber, String linkedin, String github) {
        this.name = name;
        this.email = email;
        this.phoneNumber = phoneNumber;
        this.linkedin = linkedin;
        this.github = github;
        this.skills = new ArrayList<>();
        this.projects = new ArrayList<>();
    }

    // Method to add a skill
    public void addSkill(String skill) {
        skills.add(skill);
    }

    // Method to add a project
    public void addProject(Project project) {
        projects.add(project);
    }

    // Display portfolio details
    public void displayPortfolio() {
        System.out.println("Portfolio of " + name);
        System.out.println("-------------------------------");
        System.out.println("Contact Information:");
        System.out.println("Email: " + email);
        System.out.println("Phone: " + phoneNumber);
        System.out.println("LinkedIn: " + linkedin);
        System.out.println("GitHub: " + github);
        System.out.println("\nSkills:");
        for (String skill : skills) {
            System.out.println("- " + skill);
        }
        System.out.println("\nProjects:");
        for (Project project : projects) {
            project.displayProject();
        }
    }

    public static void main(String[] args) {
        // Create a portfolio instance
        Portfolio myPortfolio = new Portfolio("NEHA KUMARI", "nnehasingh022@gmail.com", "0000000000", "linkedin.com/in/nehasingh2422", "github.com/Neha-arch616");

        // Adding skills to the portfolio
        myPortfolio.addSkill("Java");
        myPortfolio.addSkill("Python");
        myPortfolio.addSkill("HTML/CSS");
        myPortfolio.addSkill("JavaScript");
        myPortfolio.addSkill("Spring Boot");

        // Adding projects to the portfolio
        Project project1 = new Project("Project Management Tool", "A web-based tool for project management.", "https://github.com/neha/project-management-tool");
        Project project2 = new Project("Personal Portfolio", "A personal website to showcase my portfolio.", "https://github.com/johndoe/personal-portfolio");

        myPortfolio.addProject(project1);
        myPortfolio.addProject(project2);

        // Display the portfolio
        myPortfolio.displayPortfolio();
    }
}

class Project {
    private String title;
    private String description;
    private String githubLink;

    // Constructor to initialize project details
    public Project(String title, String description, String githubLink) {
        this.title = title;
        this.description = description;
        this.githubLink = githubLink;
    }

    // Method to display project details
    public void displayProject() {
        System.out.println("\nTitle: " + title);
        System.out.println("Description: " + description);
        System.out.println("GitHub Link: " + githubLink);
    }
}





//  SAMPLE OUTPUT

Portfolio of John Doe
-------------------------------
Contact Information:
Email: nnehasingh022@gmail.com
Phone: 123-456-7890
LinkedIn: linkedin.com/in/nehasingh2422
GitHub: github.com/Neha-arch616

Skills:
- Java
- Python
- HTML/CSS
- JavaScript
- Spring Boot

Projects:

Title: Project Management Tool
Description: A web-based tool for project management.
GitHub Link: https://github.com/johndoe/project-management-tool

Title: Personal Portfolio
Description: A personal website to showcase my portfolio.
GitHub Link: https://github.com/Neha-arch616/personal-portfolio
