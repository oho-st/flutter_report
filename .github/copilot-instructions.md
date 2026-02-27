# Flutter Report Project - AI Agent Guidelines

## Project Overview

This is a **multilingual technical research repository** documenting Flutter mobile development feasibility analysis. The project consists of comprehensive research reports in Japanese and Chinese, with an HTML viewer for presentation.

**Purpose**: Evaluate Flutter cross-platform development for commercial viability, focusing on AI-assisted development, cloud integration, and market opportunities.

## Repository Structure

```
flutter_report/
├── Flutter調査報告書.md      # Japanese report (624 lines) - primary research document
├── Flutter调查报告.md         # Chinese report (631 lines) - parallel translation
├── 学习计划.md                # Chinese study plan with learning milestones
├── index.html                 # Multi-tab HTML viewer for reports
├── memo                       # Technical setup notes and TODO list
├── README.md                  # Currently minimal, needs expansion
└── .github/workflows/pages.yml  # Auto-deploy to GitHub Pages on push
```

## Core Conventions

### 1. Multilingual Synchronization

- **Japanese and Chinese reports must maintain content parity** - both cover identical sections with culturally appropriate translations
- Report structure follows consistent headings (一/二/三/四/五... for both languages)
- When updating research content, **always update both language versions** unless content is language-specific
- Code examples and technical data should be identical across versions

### 2. Report Structure Pattern

Both reports follow this 6-section structure:
1. Investigation Purpose & Methodology (調査目的と方法 / 调查目的与方法)
2. AI-Assisted Development Impact (AI支援開発ツール / AI辅助开发工具)
3. Flutter Learning Path (学習パス / 学习路径) - **based on actual experience**
4. Cloud & Enterprise Integration (クラウドサービス / 云服务)
5. Freelance Platform Analysis (派遣プラットフォーム / 派遣平台)
6. Commercial Feasibility & Recommendations (商業実行可能性 / 商业可行性)

**Critical Note**: Section 3 is based on real learning experience; other sections are AI-assisted research/analysis.

### 3. Content Formatting Standards

- **Tables**: Used extensively for comparative analysis (productivity metrics, cost estimates, feature matrices)
- **Ratings**: Star ratings (★★★★★) for service support levels
- **Code blocks**: Inline for bash commands, fenced for multi-line technical content
- **Internal links**: Use markdown anchor links `[text](#section-id)` for cross-references
- **Blockquotes**: Reserve for important disclaimers (see section 1.5 in both reports)

### 4. HTML Viewer Behavior

[index.html](index.html) implements:
- Tab-based navigation between Japanese/Chinese versions
- Marked.js + DOMPurify for secure markdown rendering
- GitHub-inspired styling with responsive design
- Auto-loads from `.md` files - **no hardcoded content**

When modifying reports, HTML viewer updates automatically via fetch() - no HTML edits needed.

## Development Workflows

### Editing Reports

```bash
# Reports are plain markdown - edit directly
# Verify syntax with markdown preview
# Check cross-language consistency before committing
```

### Testing HTML Viewer Locally

```bash
cd /Users/soft-think/Documents/flutter_report
python3 -m http.server 8000
# Open http://localhost:8000
```

### Deployment

- **Auto-deploys** to GitHub Pages on every push to `main` branch
- Workflow: [.github/workflows/pages.yml](.github/workflows/pages.yml)
- Deploys entire repository root (including .md files for viewer fetch)
- No build step required - static HTML + client-side markdown rendering

## Key Technical Context

### Flutter Learning Path (from memo)

Setup sequence documented in [memo](memo):
1. Homebrew → git → VSCode (Flutter + Dart SDK extension)
2. Platform-specific: Xcode (iOS) or Android Studio + JDK (Android)
3. Verify with `flutter doctor -v`
4. Learning sequence: Dart basics (2-3d) → Flutter tutorial → Advanced (2w+)

### Report Data Sources

- **Section 3 (Learning Path)**: First-hand developer experience
- **Other sections**: AI-assisted synthesis from:
  - Stack Overflow, GitHub trends
  - 発注ナビ (freelance platform) project sampling
  - Cloud provider documentation (Firebase, AWS, Azure)

### Terminology Consistency

| English | Japanese | Chinese |
|---------|----------|---------|
| Cross-platform development | クロスプラットフォーム開発 | 跨平台开发 |
| Productivity | 生産性 | 生产力 |
| AI-assisted tools | AI支援ツール | AI辅助工具 |
| Cloud integration | クラウドサービス統合 | 云服务集成 |
| Freelance platform | 派遣プラットフォーム | 派遣平台 |

## Common Tasks

### Updating Research Content

1. Identify the section in both [Flutter調査報告書.md](Flutter調査報告書.md) and [Flutter调查报告.md](Flutter调查报告.md)
2. Make parallel edits maintaining section alignment
3. Preserve table formatting and markdown structure
4. Update dates if adding new data (report date: 2026年2月26日)

### Expanding README.md

Currently minimal - should introduce:
- Project purpose and audience (business decision-makers)
- How to view reports (GitHub Pages link + local HTML viewer)
- Report scope and disclaimer about AI-generated analysis
- Learning resources referenced

### Maintaining Study Plan

[学习计划.md](学习计划.md) tracks personal goals with checkboxes:
- Short-term (3 months): Flutter mastery, 2-3 demo projects
- Mid-term (6 months): Production app + cloud integration
- Long-term (12 months): Technical leadership + AI innovation

Update checkboxes as milestones complete.

## Pitfalls to Avoid

- **Don't** desynchronize Japanese/Chinese report content
- **Don't** embed markdown directly in index.html (it fetches dynamically)
- **Don't** commit without testing HTML viewer rendering
- **Don't** mix AI-generated claims with actual experience in Section 3
- **Don't** update report dates unless adding substantial new research
