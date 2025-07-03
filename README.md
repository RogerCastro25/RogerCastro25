class FullStackDeveloper {
  #skills = new Map();
  #projetos = [];
  
  constructor() {
    this.nome = "Roger Castro";
    this.título = "Full Stack Developer";
    this.localização = "🌎 Pelotas, RS - Brasil";
    this.experiência = "2+ anos";
    
    // 🔥 Inicializar Skills
    this.#initializeSkills();
    
    // 🎯 Status atual
    this.status = {
      disponível: true,
      buscando: ["Oportunidades remotas", "Projetos desafiadores"],
      nível: "Pleno",
      salário: "Negociável"
    };
  }
  
  // 🚀 Skills organizadas por nível
  #initializeSkills() {
    this.#skills.set("expert", ["JavaScript", "HTML", "CSS", "Git"]);
    this.#skills.set("avançado", ["React", "Node.js", "Python", "SQL"]);
    this.#skills.set("intermediário", ["TypeScript", "Next.js", "MongoDB"]);
    this.#skills.set("aprendendo", ["DevOps", "Kubernetes", "GraphQL"]);
  }
  
  // 🎯 Getter para skills
  get skills() {
    return Object.fromEntries(this.#skills);
  }
  
  // 📊 Método para mostrar progresso
  mostrarProgresso() {
    const progresso = {
      "Frontend": "████████████████████ 100%",
      "Backend": "████████████████▒▒▒▒ 80%",
      "DevOps": "████████▒▒▒▒▒▒▒▒▒▒▒▒ 40%",
      "Mobile": "██████████▒▒▒▒▒▒▒▒▒▒ 50%"
    };
    
    return progresso;
  }
  
  // 🔥 Método assíncrono para projetos
  async buscarProjetos() {
    return new Promise(resolve => {
      setTimeout(() => {
        resolve([
          "🛒 E-commerce com React + Node.js",
          "🤖 Chatbot com IA integrada",
          "📱 App mobile com React Native",
          "☁️ Deploy automatizado com Docker"
        ]);
      }, 1000);
    });
  }
  
  // 🚀 Método para conectar
  async conectar(plataforma = "email") {
    const contatos = {
      email: "pedrocastro.roger23@gmail.com",
      linkedin: "pedro-castro-6b453595",
      github: "RogerCAstro25",
      discord: "pedro_castro23"
    };
    
    return `📬 Me encontre no ${plataforma}: ${contatos[plataforma]}`;
  }
  
  // 💡 Método para objetivos
  proximosObjetivos() {
    return [
      "🎯 Tornar-se Tech Lead",
      "🌟 Contribuir para Open Source",
      "📚 Mentorear outros devs",
      "🚀 Criar minha própria startup"
    ];
  }
}

// 🔥 Instância do desenvolvedor
const roger = new FullStackDeveloper();

// 🎯 Executar apresentação
console.log(`👋 Olá! Eu sou ${roger.nome}`);
console.log("📊 Meu progresso atual:");
console.table(roger.mostrarProgresso());
