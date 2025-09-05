# Espanso Prompt Dataset

A well-organized repository for managing [Espanso](https://espanso.org/) text expansion prompts with automatic configuration generation.

## 📁 Repository Structure

```
Espanso-Prompt-Dataset/
├── prompts/                    # Individual prompt files organized by category
│   ├── coding/                # Programming-related prompts
│   │   └── development.yaml   # Code templates, git commits, etc.
│   ├── productivity/          # Productivity and work-related prompts
│   │   └── email.yaml        # Email templates and responses
│   ├── personal/             # Personal information and common phrases
│   │   └── common.yaml       # Contact info, dates, meeting notes
│   └── text-expansion/       # Abbreviations and text shortcuts
│       └── abbreviations.yaml # Common abbreviations and typo fixes
├── scripts/                  # Utility scripts
│   └── generate_main_config.py # Script to combine all prompts
├── .github/workflows/        # GitHub Actions workflows
│   └── generate-config.yml   # Auto-generates main-base.yaml
├── main-base.yaml           # Auto-generated combined configuration
├── requirements.txt         # Python dependencies
└── README.md               # This file
```

## 🚀 How It Works

1. **Individual Prompt Files**: Create and organize your prompts in separate YAML files within the `prompts/` directory
2. **Automatic Generation**: GitHub Actions automatically combines all prompt files into a single `main-base.yaml`
3. **Easy Management**: Edit individual files for specific categories without dealing with one massive configuration file

## 📝 Adding New Prompts

### 1. Choose the Right Category

- **coding/**: Programming templates, git commits, code snippets
- **productivity/**: Email templates, meeting notes, work-related shortcuts
- **personal/**: Personal information, common phrases, dates
- **text-expansion/**: Abbreviations, typo corrections, common expansions

### 2. Create or Edit a YAML File

Each prompt file should follow this structure:

```yaml
matches:
  - trigger: ":example"
    replace: "This is an example expansion"
    
  - trigger: ":template"
    replace: |
      Multi-line template
      with {{placeholder}} variables
      
  - trigger: ":dynamic"
    replace: "Today is {{date}}"
    vars:
      - name: date
        type: date
        params:
          format: "%Y-%m-%d"
```

### 3. Automatic Processing

When you push changes to the `main` branch:
- GitHub Actions detects changes in `prompts/**/*.yaml` files
- Runs the generation script to create `main-base.yaml`
- Commits the updated configuration automatically

## 🔧 Manual Generation

To generate the main configuration locally:

```bash
# Install dependencies
pip install -r requirements.txt

# Run the generation script
python scripts/generate_main_config.py
```

## 📋 Using with Espanso

1. **Copy the generated file**: Take the `main-base.yaml` file and copy it to your Espanso configuration directory
2. **Espanso config location**:
   - Linux: `~/.config/espanso/match/`
   - macOS: `~/Library/Application Support/espanso/match/`
   - Windows: `%APPDATA%\espanso\match\`

3. **Reload Espanso**: Run `espanso restart` to load the new configuration

## 📂 Example Prompts Included

### Coding (`prompts/coding/development.yaml`)
- `:pydef` - Python function template
- `:jsfunction` - JavaScript function template
- `:gitfix` - Git commit message for fixes
- `:tryexcept` - Python try/except block

### Productivity (`prompts/productivity/email.yaml`)
- `:emailmeet` - Meeting request template
- `:emailfollow` - Follow-up email template
- `:ack` - Quick acknowledgment response

### Personal (`prompts/personal/common.yaml`)
- `:today` - Current date
- `:myemail` - Your email address
- `:meetingnotes` - Meeting notes template

### Text Expansion (`prompts/text-expansion/abbreviations.yaml`)
- `:btw` → "by the way"
- `:fyi` → "for your information"
- Common typo corrections (teh → the, etc.)

## 🔄 Workflow

1. **Add/Edit Prompts**: Modify files in the `prompts/` directory
2. **Commit Changes**: Push to the `main` branch
3. **Automatic Generation**: GitHub Actions creates updated `main-base.yaml`
4. **Use Configuration**: Copy the generated file to your Espanso installation

## 🎯 Benefits

- **Organization**: Keep related prompts together in logical files
- **Maintainability**: Edit specific categories without touching others
- **Automation**: No manual file combination required
- **Version Control**: Track changes to individual prompt categories
- **Collaboration**: Multiple people can work on different prompt categories

## 🛠️ Customization

### Adding New Categories

1. Create a new directory under `prompts/`
2. Add YAML files with your prompts
3. The generation script will automatically include them

### Modifying the Generation Script

The `scripts/generate_main_config.py` file can be customized to:
- Change the output format
- Add additional processing
- Include metadata or comments
- Filter specific prompt types

## 📄 License

This repository template is available for anyone to use and modify for their own Espanso prompt management.

## 🤝 Contributing

Feel free to submit issues and enhancement requests! This is a template repository, so you can:
- Fork it for your own use
- Suggest improvements to the automation
- Share useful prompt categories

## 📚 Resources

- [Espanso Official Documentation](https://espanso.org/docs/)
- [Espanso Configuration Guide](https://espanso.org/docs/configuration/)
- [YAML Syntax Reference](https://yaml.org/spec/1.2/spec.html)
