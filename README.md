# Cheshire Framework - Umbrella Repository

This is the umbrella repository for the Cheshire framework ecosystem, containing multiple related projects managed as git submodules.

## Repository Structure

This repository contains the following projects:

- **[cheshire-prototype](https://github.com/halimchaibi/cheshire-prototype)** - The Cheshire framework (core framework implementation)
- **[cheshire-blog-app](https://github.com/halimchaibi/cheshire-blog-app)** - Reference implementation demonstrating Cheshire framework capabilities

## Cloning the Repository

To clone this repository with all submodules, use one of the following methods:

### Method 1: Clone with submodules (recommended)
```bash
git clone --recursive https://github.com/halimchaibi/cheshire-framework.git
```

### Method 2: Clone then initialize submodules
```bash
git clone https://github.com/halimchaibi/cheshire-framework.git
cd cheshire-framework
git submodule update --init --recursive
```
## 📦 Releases

| Version | Status | Source |
|--------|--------|--------|
| [`v1.0.0-alpha.1` ](https://github.com/halimchaibi/cheshire-framework/releases/tag/v1.0.0-alpha.1)| Latest | Direct Clone |

## 🗂 Project Board

Project planning, progress tracking, and roadmap are managed on the GitHub Project board:

👉 https://github.com/users/halimchaibi/projects/2

## Working with Submodules

### Updating Submodules

To update all submodules to their latest commits:
```bash
git submodule update --remote
```

To update a specific submodule:
```bash
git submodule update --remote cheshire-blog-app
```

### Making Changes in Submodules

1. Navigate to the submodule directory:
   ```bash
   cd cheshire-blog-app
   ```

2. Make your changes and commit them in the submodule's repository:
   ```bash
   git add .
   git commit -m "Your commit message"
   git push
   ```

3. Return to the umbrella repository and update the submodule reference:
   ```bash
   cd ..
   git add cheshire-blog-app
   git commit -m "Update cheshire-blog-app submodule"
   git push
   ```

### Pulling Latest Changes

When pulling changes to the umbrella repository, you may need to update submodules:
```bash
git pull
git submodule update --init --recursive
```

## Individual Project Repositories

Each submodule maintains its own independent repository:

- **cheshire-blog-app**: https://github.com/halimchaibi/cheshire-blog-app
- **cheshire-prototype**: https://github.com/halimchaibi/cheshire-prototype

You can work directly in these repositories or through the umbrella repository.

## Development Workflow

1. Clone the umbrella repository with submodules
2. Navigate to the project you want to work on
3. Create a branch in the submodule repository for your changes
4. Make changes, commit, and push to the submodule repository
5. Update the umbrella repository to reference the new commit

## Notes

- The umbrella repository tracks specific commits of each submodule
- Each submodule can be developed independently
- Changes to submodules do not automatically update the umbrella repository - you must commit the submodule reference update

## 🛠 Development Methodology
**This project was built using a Human-in-the-Loop AI workflow, leveraging LLMs as a force-multiplier for development velocity**

## License

This project is licensed under the [PolyForm Noncommercial License 1.0.0](https://polyformproject.org/licenses/noncommercial/1.0.0/).

See the [LICENSE](LICENSE) file for the full license text.


