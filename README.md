import React from 'react';
import { motion, AnimatePresence } from 'framer-motion';
import { FaLinkedin, FaEnvelope, FaGithub } from 'react-icons/fa';

// Full single-file animated portfolio page
// Usage: place this file in a React or Next.js project (e.g. pages/index.js or src/components/PortfolioPage.jsx)
// Dependencies: framer-motion, react-icons, tailwindcss

const projects = [
  {
    title: 'Brain Tumor Detection System',
    description:
      'Production medical AI: MRI-based brain tumor classification using EfficientNetB0. Dockerized microservices and HIPAA-conscious pipelines.',
    tech: ['TensorFlow', 'Keras', 'Flask', 'Docker'],
    href: 'https://github.com/bilal-0046/brain-tumor-detection',
  },
  {
    title: 'AI-Powered Interactive Portfolio',
    description:
      'Conversational portfolio with natural-language navigation, perfect Lighthouse scores and edge deployment.',
    tech: ['React', 'Dialogflow', 'Tailwind'],
    href: 'https://github.com/bilal-0046/portfolio',
  },
  {
    title: 'Graph Cycle Detection',
    description:
      'Algorithm engineering: DFS-based cycle detection with extensive tests and O(V + E) complexity.',
    tech: ['Java', 'Algorithms'],
    href: 'https://github.com/bilal-0046/graph-cycle-detection',
  },
];

const achievements = [
  'Deployed clinical-grade brain tumor detection system (92% accuracy)',
  'TensorFlow Open Source Contributor',
  'Google Certified: TensorFlow Developer & Data Science Professional',
  'Healthcare AI systems serving active medical facilities',
  '100/100 Lighthouse score on production web applications',
];

const timeline = [
  { quarter: 'Q4 2025', items: ['Federated Learning Integration (In Progress)', 'Flutter Medical Diagnostics App (In Progress)'] },
  { quarter: '2025', items: ['Demystifying Deep Learning blog series (Active)', 'Open Source ML Contributions (Ongoing)'] },
];

const cardVariants = {
  hidden: { opacity: 0, y: 24, scale: 0.98 },
  visible: { opacity: 1, y: 0, scale: 1, transition: { duration: 0.5 } },
  hover: { scale: 1.02, y: -6, transition: { duration: 0.25 } },
};

export default function AnimatedPortfolioPage() {
  return (
    <div className="min-h-screen bg-gradient-to-br from-gray-900 via-black to-gray-800 text-white antialiased">
      {/* Background subtle grid + vignette */}
      <div className="absolute inset-0 pointer-events-none overflow-hidden">
        <div className="absolute inset-0 bg-gradient-to-b from-transparent to-black opacity-30" />
        <svg
          className="absolute inset-0 w-full h-full"
          preserveAspectRatio="none"
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 800 600"
        >
          <defs>
            <linearGradient id="g" x1="0" x2="1">
              <stop offset="0%" stopColor="#00f" stopOpacity="0.03" />
              <stop offset="100%" stopColor="#8a2be2" stopOpacity="0.02" />
            </linearGradient>
          </defs>
          <rect width="800" height="600" fill="url(#g)" />
        </svg>
      </div>

      <main className="relative z-10 max-w-6xl mx-auto px-6 lg:px-8 py-16">
        {/* Header / Hero */}
        <section className="flex flex-col lg:flex-row items-start gap-8">
          <motion.div
            initial={{ opacity: 0, x: -40 }}
            animate={{ opacity: 1, x: 0 }}
            transition={{ duration: 0.8 }}
            className="flex-1"
          >
            <h1 className="text-5xl lg:text-6xl font-extrabold leading-tight">
              Muhammad Bilal
            </h1>
            <motion.p
              initial={{ opacity: 0 }}
              animate={{ opacity: 1 }}
              transition={{ delay: 0.3, duration: 0.8 }}
              className="mt-4 text-xl max-w-2xl"
            >
              Artificial Intelligence Engineer • Machine Learning Researcher • Healthcare AI Innovator
            </motion.p>

            <div className="mt-6 flex flex-wrap gap-3">
              <a
                href="mailto:muhammadbilal0046@gmail.com"
                className="inline-flex items-center gap-2 px-5 py-2 rounded-2xl bg-gradient-to-r from-blue-600 to-teal-500 hover:scale-105 transform transition"
              >
                <FaEnvelope /> Contact
              </a>

              <a
                href="https://www.linkedin.com/in/muhammadbilal0046"
                className="inline-flex items-center gap-2 px-5 py-2 rounded-2xl bg-gray-800 border border-gray-700 hover:border-white transition"
              >
                <FaLinkedin /> LinkedIn
              </a>

              <a
                href="https://github.com/bilal-0046"
                className="inline-flex items-center gap-2 px-5 py-2 rounded-2xl bg-gray-800 border border-gray-700 hover:border-white transition"
              >
                <FaGithub /> GitHub
              </a>
            </div>

            <div className="mt-8 grid grid-cols-1 sm:grid-cols-2 gap-4">
              <motion.div
                initial={{ opacity: 0, y: 12 }}
                animate={{ opacity: 1, y: 0 }}
                transition={{ delay: 0.2 }}
                className="p-5 rounded-2xl bg-gradient-to-br from-white/5 to-white/3 border border-white/5"
              >
                <h3 className="text-sm text-slate-300">Core Competencies</h3>
                <ul className="mt-2 text-sm leading-relaxed text-slate-200">
                  <li>Deep Learning Architecture Design & Optimization</li>
                  <li>Computer Vision & Medical Image Analysis</li>
                  <li>Federated Learning & Privacy-Preserving AI</li>
                  <li>Full-Stack ML Pipeline Development</li>
                </ul>
              </motion.div>

              <motion.div
                initial={{ opacity: 0, y: 12 }}
                animate={{ opacity: 1, y: 0 }}
                transition={{ delay: 0.35 }}
                className="p-5 rounded-2xl bg-gradient-to-br from-white/5 to-white/3 border border-white/5"
              >
                <h3 className="text-sm text-slate-300">Current Focus</h3>
                <p className="mt-2 text-sm text-slate-200">
                  Privacy-preserving ML for medical imaging, production-ready deployment, and federated
                  learning integration.
                </p>
              </motion.div>
            </div>
          </motion.div>

          {/* Right column - achievements card */}
          <motion.aside
            initial={{ opacity: 0, x: 40 }}
            animate={{ opacity: 1, x: 0 }}
            transition={{ duration: 0.8 }}
            className="w-full lg:w-96"
          >
            <div className="p-6 rounded-3xl bg-gradient-to-br from-white/4 to-white/2 border border-white/6">
              <h4 className="text-lg font-semibold">Key Achievements</h4>
              <ul className="mt-4 space-y-3 text-sm text-slate-200">
                {achievements.slice(0, 5).map((a, i) => (
                  <li key={i} className="flex gap-3 items-start">
                    <span className="mt-1 text-teal-300 font-semibold">✓</span>
                    <span>{a}</span>
                  </li>
                ))}
              </ul>
            </div>
          </motion.aside>
        </section>

        {/* Projects */}
        <section className="mt-16">
          <motion.h2
            initial={{ opacity: 0, y: 8 }}
            animate={{ opacity: 1, y: 0 }}
            className="text-2xl font-bold"
          >
            Featured Projects
          </motion.h2>

          <div className="mt-6 grid grid-cols-1 md:grid-cols-3 gap-6">
            {projects.map((p, idx) => (
              <motion.a
                key={p.title}
                href={p.href}
                target="_blank"
                rel="noreferrer"
                initial="hidden"
                whileInView="visible"
                whileHover="hover"
                viewport={{ once: true, amount: 0.2 }}
                variants={cardVariants}
                className="block p-6 rounded-2xl bg-gradient-to-br from-white/3 to-white/4 border border-white/6 shadow-lg"
              >
                <h3 className="text-lg font-semibold">{p.title}</h3>
                <p className="mt-3 text-sm text-slate-200">{p.description}</p>
                <div className="mt-4 flex flex-wrap gap-2">
                  {p.tech.map((t) => (
                    <span
                      key={t}
                      className="text-xs px-2 py-1 rounded-full bg-white/5 border border-white/6"
                    >
                      {t}
                    </span>
                  ))}
                </div>
              </motion.a>
            ))}
          </div>
        </section>

        {/* Timeline / Roadmap */}
        <section className="mt-16">
          <motion.h2 initial={{ opacity: 0, y: 8 }} animate={{ opacity: 1, y: 0 }} className="text-2xl font-bold">
            Q4 2025 Roadmap
          </motion.h2>

          <div className="mt-6 grid grid-cols-1 md:grid-cols-2 gap-6">
            {timeline.map((t) => (
              <motion.div
                key={t.quarter}
                initial={{ opacity: 0, y: 12 }}
                animate={{ opacity: 1, y: 0 }}
                transition={{ duration: 0.5 }}
                className="p-6 rounded-2xl bg-gradient-to-br from-white/5 to-white/3 border border-white/6"
              >
                <h4 className="font-semibold">{t.quarter}</h4>
                <ul className="mt-3 text-sm text-slate-200 space-y-2">
                  {t.items.map((it, i) => (
                    <li key={i} className="flex items-start gap-3">
                      <span className="mt-1 text-indigo-300">●</span>
                      <span>{it}</span>
                    </li>
                  ))}
                </ul>
              </motion.div>
            ))}
          </div>
        </section>

        {/* Achievements animated list */}
        <section className="mt-16">
          <motion.h2 initial={{ opacity: 0, y: 8 }} animate={{ opacity: 1, y: 0 }} className="text-2xl font-bold">
            Achievements & Recognition
          </motion.h2>

          <motion.div className="mt-6 grid grid-cols-1 sm:grid-cols-2 gap-4">
            {achievements.map((a, i) => (
              <motion.div
                key={i}
                whileHover={{ scale: 1.02 }}
                initial={{ opacity: 0, y: 8 }}
                animate={{ opacity: 1, y: 0 }}
                transition={{ delay: i * 0.08 }}
                className="p-4 rounded-xl bg-gradient-to-br from-white/3 to-white/2 border border-white/6"
              >
                <p className="text-sm">{a}</p>
              </motion.div>
            ))}
          </motion.div>
        </section>

        {/* Contact / Footer */}
        <section className="mt-16 mb-12">
          <motion.h2 initial={{ opacity: 0, y: 8 }} animate={{ opacity: 1, y: 0 }} className="text-2xl font-bold">
            Let's collaborate
          </motion.h2>

          <motion.div
            initial={{ opacity: 0 }}
            animate={{ opacity: 1 }}
            transition={{ delay: 0.2 }}
            className="mt-6 p-6 rounded-2xl bg-gradient-to-br from-white/4 to-white/3 border border-white/6 flex flex-col sm:flex-row gap-6 items-center"
          >
            <div className="flex-1">
              <p className="text-sm text-slate-200">Interested in research collaboration, consulting, or open source work? Reach out!</p>
              <div className="mt-4 flex items-center gap-3">
                <a href="mailto:muhammadbilal0046@gmail.com" className="inline-flex items-center gap-2 px-5 py-2 rounded-2xl bg-teal-500">
                  <FaEnvelope /> Email
                </a>
                <a href="https://www.linkedin.com/in/muhammadbilal0046" className="inline-flex items-center gap-2 px-5 py-2 rounded-2xl bg-gray-800 border border-white/6">
                  <FaLinkedin /> LinkedIn
                </a>
              </div>
            </div>

            <div className="w-full sm:w-64 text-center">
              <p className="text-xs text-slate-300">Quick Contact</p>
              <a href="mailto:muhammadbilal0046@gmail.com" className="mt-2 inline-block text-sm font-medium">muhammadbilal0046@gmail.com</a>
            </div>
          </motion.div>

          <footer className="mt-6 text-center text-xs text-slate-400">© {new Date().getFullYear()} Muhammad Bilal — Powered by curiosity, driven by impact</footer>
        </section>
      </main>

      {/* small floating dot grid for depth */}
      <div className="pointer-events-none fixed right-6 bottom-6 opacity-40 hidden md:block">
        <svg width="120" height="120" viewBox="0 0 120 120" fill="none" xmlns="http://www.w3.org/2000/svg">
          <defs>
            <linearGradient id="lg" x1="0" x2="1">
              <stop offset="0%" stopColor="#00f" stopOpacity="0.2" />
              <stop offset="100%" stopColor="#8a2be2" stopOpacity="0.15" />
            </linearGradient>
          </defs>
          <rect width="120" height="120" fill="url(#lg)" rx="12" />
        </svg>
      </div>
    </div>
  );
}
