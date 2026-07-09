<!-- ========================= HERO ========================= -->

<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&height=250&color=0:000000,50:111827,100:0f172a&text=Sayan%20Duary&fontSize=50&color=00F5FF&animation=fadeIn&fontAlignY=35&desc=Full%20Stack%20Developer%20|%20Backend%20Engineer%20|%20Generative%20AI%20Developer&descAlignY=56"/>

<br>

<img src="https://readme-typing-svg.herokuapp.com?font=JetBrains+Mono&weight=500&size=24&duration=2500&pause=900&color=00F5FF&background=00000000&center=true&vCenter=true&width=850&lines=Full+Stack+Developer;Backend+Engineer;Generative+AI+Developer;Building+Scalable+Applications;Node.js+%7C+React+%7C+Next.js+%7C+TypeScript;LangChain+%7C+RAG+Systems;Docker+%7C+Kubernetes;Always+Learning+Something+New+%F0%9F%9A%80" />

<br><br>

<img src="https://img.shields.io/github/followers/sayanduary?style=for-the-badge&color=00F5FF&labelColor=000000">
<img src="https://img.shields.io/github/stars/sayanduary?style=for-the-badge&color=7C3AED&labelColor=000000">
<img src="https://komarev.com/ghpvc/?username=sayanduary&style=for-the-badge&color=00F5FF&label=PROFILE+VIEWS">

</div>

---

<!-- ========================= ABOUT ========================= -->

## 👨‍💻 About Me

```javascript
const sayan = {
    name: "Sayan Duary",
    role: "Full Stack Developer",
    specialization: [
        "Backend Development",
        "REST API Development",
        "Generative AI",
        "RAG Systems",
        "System Design"
    ],
    currentlyExploring: [
        "LangChain & RAG pipelines",
        "Kubernetes orchestration",
        "System design fundamentals"
    ],
    motto: "Turning Ideas into Scalable Software 🚀"
}
```

---

<!-- ========================= TECH STACK ========================= -->

## 🛠️ Tech Stack

**Languages**

<div align="center">
<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" />
<img src="https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white" />
<img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" />
<img src="https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white" />
</div>

**Frontend**

<div align="center">
<img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" />
<img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white" />
<img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white" />
</div>

**Backend**

<div align="center">
<img src="https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white" />
<img src="https://img.shields.io/badge/Express.js-404D59?style=for-the-badge&logo=express&logoColor=white" />
</div>

**Databases**

<div align="center">
<img src="https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white" />
<img src="https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white" />
<img src="https://img.shields.io/badge/MySQL-00000F?style=for-the-badge&logo=mysql&logoColor=white" />
</div>

**Generative AI / LLM**

<div align="center">
<img src="https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white" />
<img src="https://img.shields.io/badge/RAG_Systems-4B5563?style=for-the-badge&logo=databricks&logoColor=white" />
</div>

**DevOps & Systems**

<div align="center">
<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
<img src="https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white" />
<img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" />
</div>

**Tools**

<div align="center">
<img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" />
<img src="https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white" />
<img src="https://img.shields.io/badge/Prisma-2D3748?style=for-the-badge&logo=prisma&logoColor=white" />
</div>

**Core Computer Science**

<div align="center">
<img src="https://img.shields.io/badge/Data_Structures_%26_Algorithms-000000?style=for-the-badge" />
<img src="https://img.shields.io/badge/System_Design-000000?style=for-the-badge" />
<img src="https://img.shields.io/badge/Networking-000000?style=for-the-badge" />
<img src="https://img.shields.io/badge/Operating_Systems-000000?style=for-the-badge" />
</div>

---

<!-- ========================= SAMPLE DOCKERFILE ========================= -->

## 🐳 Sample Multi-stage Dockerfile (Node.js App)

```dockerfile
# Multi-stage Dockerfile for Node.js App
FROM node:18-alpine AS builder

WORKDIR /app

# Copy package files
COPY package*.json ./
COPY prisma ./prisma/

# Install dependencies
RUN npm ci --only=production

# Copy source code
COPY . .

# Build application
RUN npm run build

# Production stage
FROM node:18-alpine

WORKDIR /app

# Copy built application
COPY --from=builder /app/dist ./dist
COPY --from=builder /app/node_modules ./node_modules
COPY --from=builder /app/package*.json ./
COPY --from=builder /app/prisma ./prisma

# Create non-root user
RUN addgroup -g 1001 -S nodejs && \
    adduser -S nodejs -u 1001 && \
    chown -R nodejs:nodejs /app

USER nodejs

EXPOSE 3000

CMD ["node", "dist/main.js"]
```

---

<!-- ========================= GITHUB STATS ========================= -->

## 📊 GitHub Stats

<div align="center">
<img src="https://github-readme-streak-stats.herokuapp.com/?user=sayanduary&theme=radical&background=0d1117&stroke=00F5FF&ring=7C3AED&fire=00F5FF&currStreakNum=00F5FF&sideNums=00F5FF&currStreakLabel=7C3AED&sideLabels=7C3AED&dates=00F5FF" />
</div>

<div align="center">
<img src="https://github-readme-stats.vercel.app/api/wakatime?username=sayanduary&theme=radical&bg_color=0d1117&title_color=00F5FF&text_color=c9d1d9&custom_title=Weekly%20Coding%20Activity" />
</div>

---

<!-- ========================= CONNECT ========================= -->

## 🔗 Connect With Me

<div align="center">
<a href="https://www.linkedin.com/in/sayan-duary/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
<a href="mailto:sayanduary@gmail.com"><img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white"/></a>
<a href="https://sayanduary.vercel.app/"><img src="https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white"/></a>
</div>

<div align="center">
<img src="https://capsule-render.vercel.app/api?type=waving&height=150&color=0:000000,50:111827,100:0f172a&text=Thanks%20for%20Visiting!&fontSize=30&color=00F5FF&animation=fadeIn&fontAlignY=50&section=footer"/>
</div>
