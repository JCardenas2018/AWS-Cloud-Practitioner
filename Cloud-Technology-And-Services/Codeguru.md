# AWS CodeGuru: Simple Examples

AWS CodeGuru helps improve code quality and performance using automated analysis and machine learning. It consists of:

- **Reviewer**: analyzes Java/Python pull requests and suggests improvements  
- **Profiler**: profiles your production application and highlights CPU hotspots  
- **Security**: detects security vulnerabilities in your code  

---

## 1. CodeGuru Reviewer (Java)

**Issue:** Manual resource handling can leak connections.

```java
public void readFile(String path) throws IOException {
    FileInputStream fis = new FileInputStream(path);
    // ... processing ...
    fis.close();
}
