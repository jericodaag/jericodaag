import React from 'react';
import { Code, Coffee, Database, GitBranch, Globe, Server, Tools } from 'lucide-react';

const DeveloperProfile = () => {
  const jerico = {
    role: "Full Stack Developer",
    code: ["JavaScript", "PHP", "Python", "SQL", "HTML", "CSS"],
    technologies: {
      frontEnd: {
        js: ["React.js"],
        css: ["Tailwind CSS", "Bootstrap"]
      },
      backEnd: {
        js: ["Node.js", "Express.js"],
        php: ["Laravel"]
      },
      databases: ["MySQL", "MongoDB"],
      tools: ["Git", "GitHub", "VS Code", "Postman"]
    },
    currentFocus: "Building scalable web applications",
    funFact: "I code better with coffee ☕"
  };

  return (
    <div className="max-w-3xl mx-auto p-6 bg-white rounded-lg shadow-lg">
      <div className="space-y-6">
        {/* Header */}
        <div className="text-center border-b pb-6">
          <h1 className="text-3xl font-bold text-gray-800">{jerico.role}</h1>
          <p className="mt-2 text-gray-600">{jerico.currentFocus}</p>
        </div>

        {/* Programming Languages */}
        <div className="space-y-2">
          <div className="flex items-center gap-2 text-gray-700">
            <Code className="w-5 h-5" />
            <h2 className="text-lg font-semibold">Programming Languages</h2>
          </div>
          <div className="flex flex-wrap gap-2">
            {jerico.code.map((lang) => (
              <span key={lang} className="px-3 py-1 bg-blue-100 text-blue-700 rounded-full text-sm">
                {lang}
              </span>
            ))}
          </div>
        </div>

        {/* Frontend */}
        <div className="space-y-2">
          <div className="flex items-center gap-2 text-gray-700">
            <Globe className="w-5 h-5" />
            <h2 className="text-lg font-semibold">Frontend Technologies</h2>
          </div>
          <div className="flex flex-wrap gap-2">
            {jerico.technologies.frontEnd.js.concat(jerico.technologies.frontEnd.css).map((tech) => (
              <span key={tech} className="px-3 py-1 bg-green-100 text-green-700 rounded-full text-sm">
                {tech}
              </span>
            ))}
          </div>
        </div>

        {/* Backend */}
        <div className="space-y-2">
          <div className="flex items-center gap-2 text-gray-700">
            <Server className="w-5 h-5" />
            <h2 className="text-lg font-semibold">Backend Technologies</h2>
          </div>
          <div className="flex flex-wrap gap-2">
            {[...jerico.technologies.backEnd.js, ...jerico.technologies.backEnd.php].map((tech) => (
              <span key={tech} className="px-3 py-1 bg-purple-100 text-purple-700 rounded-full text-sm">
                {tech}
              </span>
            ))}
          </div>
        </div>

        {/* Databases */}
        <div className="space-y-2">
          <div className="flex items-center gap-2 text-gray-700">
            <Database className="w-5 h-5" />
            <h2 className="text-lg font-semibold">Databases</h2>
          </div>
          <div className="flex flex-wrap gap-2">
            {jerico.technologies.databases.map((db) => (
              <span key={db} className="px-3 py-1 bg-yellow-100 text-yellow-700 rounded-full text-sm">
                {db}
              </span>
            ))}
          </div>
        </div>

        {/* Tools */}
        <div className="space-y-2">
          <div className="flex items-center gap-2 text-gray-700">
            <Tools className="w-5 h-5" />
            <h2 className="text-lg font-semibold">Tools</h2>
          </div>
          <div className="flex flex-wrap gap-2">
            {jerico.technologies.tools.map((tool) => (
              <span key={tool} className="px-3 py-1 bg-red-100 text-red-700 rounded-full text-sm">
                {tool}
              </span>
            ))}
          </div>
        </div>

        {/* Fun Fact */}
        <div className="mt-6 text-center">
          <div className="flex items-center justify-center gap-2 text-gray-600">
            <Coffee className="w-5 h-5" />
            <p className="text-lg">{jerico.funFact}</p>
          </div>
        </div>
      </div>
    </div>
  );
};

export default DeveloperProfile;
