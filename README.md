import React from 'react';
import { User, Code, Database, Smartphone, Globe, Phone, Mail, Linkedin, Instagram, MessageCircle } from 'lucide-react';

const ProfileApp = () => {
  const technologies = [
    { name: 'JavaScript', color: 'bg-yellow-500' },
    { name: 'TypeScript', color: 'bg-blue-600' },
    { name: 'React', color: 'bg-cyan-500' },
    { name: 'Flutter', color: 'bg-sky-500' },
    { name: 'Node.js', color: 'bg-green-600' },
    { name: 'Laravel', color: 'bg-red-500' },
    { name: 'Vue.js', color: 'bg-emerald-500' },
    { name: 'Firebase', color: 'bg-orange-500' },
    { name: 'MySQL', color: 'bg-blue-700' },
    { name: 'PHP', color: 'bg-indigo-600' },
    { name: 'Tailwind CSS', color: 'bg-teal-500' },
    { name: 'Bootstrap', color: 'bg-purple-600' }
  ];

  const skills = [
    { icon: <Globe className="w-5 h-5" />, title: 'Web Development', desc: 'React, Vue.js, Laravel' },
    { icon: <Smartphone className="w-5 h-5" />, title: 'Mobile Development', desc: 'Flutter, React Native' },
    { icon: <Database className="w-5 h-5" />, title: 'Backend', desc: 'Node.js, Express.js, PHP' },
    { icon: <Code className="w-5 h-5" />, title: 'E-commerce', desc: 'WordPress, Shopify' }
  ];

  const socialLinks = [
    { icon: <Linkedin className="w-5 h-5" />, name: 'LinkedIn', color: 'bg-blue-600' },
    { icon: <Instagram className="w-5 h-5" />, name: 'Instagram', color: 'bg-pink-600' },
    { icon: <MessageCircle className="w-5 h-5" />, name: 'WhatsApp', color: 'bg-green-500' }
  ];

  return (
    <div className="min-h-screen bg-gradient-to-br from-slate-900 via-purple-900 to-slate-900">
      {/* Header */}
      <div className="relative overflow-hidden">
        <div className="absolute inset-0 bg-gradient-to-r from-purple-600/20 to-cyan-600/20"></div>
        <div className="relative px-6 py-8">
          <div className="text-center">
            <div className="w-32 h-32 mx-auto mb-6 rounded-full bg-gradient-to-r from-purple-500 to-cyan-500 p-1">
              <div className="w-full h-full rounded-full bg-slate-800 flex items-center justify-center">
                <User className="w-16 h-16 text-white" />
              </div>
            </div>
            <h1 className="text-3xl font-bold text-white mb-2">Mohamed Seddik</h1>
            <p className="text-cyan-300 text-lg">Full Stack Developer</p>
            <div className="flex justify-center space-x-4 mt-4">
              {socialLinks.map((social, index) => (
                <button
                  key={index}
                  className={`${social.color} p-3 rounded-full shadow-lg transform hover:scale-105 transition-all duration-200`}
                >
                  {social.icon}
                </button>
              ))}
            </div>
          </div>
        </div>
      </div>

      {/* Welcome Message */}
      <div className="px-6 py-4">
        <div className="bg-slate-800/50 backdrop-blur-sm rounded-xl p-6 border border-slate-700">
          <h2 className="text-2xl font-bold text-white mb-4 flex items-center">
            <span className="text-2xl mr-2">👋</span>
            Welcome to my profile!
          </h2>
          <p className="text-slate-300 leading-relaxed">
            I am a passionate web and mobile developer, specializing in building high-performance and user-friendly applications.
          </p>
        </div>
      </div>

      {/* Skills Section */}
      <div className="px-6 py-4">
        <h3 className="text-xl font-bold text-white mb-4 flex items-center">
          <Code className="w-6 h-6 mr-2 text-cyan-400" />
          What I Do
        </h3>
        <div className="grid grid-cols-1 gap-4">
          {skills.map((skill, index) => (
            <div key={index} className="bg-slate-800/50 backdrop-blur-sm rounded-xl p-4 border border-slate-700">
              <div className="flex items-center mb-2">
                <div className="text-cyan-400 mr-3">
                  {skill.icon}
                </div>
                <h4 className="font-semibold text-white">{skill.title}</h4>
              </div>
              <p className="text-slate-400 text-sm">{skill.desc}</p>
            </div>
          ))}
        </div>
      </div>

      {/* Technologies */}
      <div className="px-6 py-4">
        <h3 className="text-xl font-bold text-white mb-4 flex items-center">
          <Database className="w-6 h-6 mr-2 text-cyan-400" />
          Technologies & Tools
        </h3>
        <div className="grid grid-cols-2 gap-3">
          {technologies.map((tech, index) => (
            <div key={index} className="bg-slate-800/50 backdrop-blur-sm rounded-lg p-3 border border-slate-700">
              <div className="flex items-center">
                <div className={`w-3 h-3 rounded-full ${tech.color} mr-3`}></div>
                <span className="text-white font-medium text-sm">{tech.name}</span>
              </div>
            </div>
          ))}
        </div>
      </div>

      {/* Contact Section */}
      <div className="px-6 py-4">
        <h3 className="text-xl font-bold text-white mb-4 flex items-center">
          <Phone className="w-6 h-6 mr-2 text-cyan-400" />
          Get In Touch
        </h3>
        <div className="bg-slate-800/50 backdrop-blur-sm rounded-xl p-6 border border-slate-700">
          <p className="text-slate-300 mb-4">
            I love tackling technical challenges and exploring new technologies to optimize my projects. Feel free to reach out for collaboration! 🚀
          </p>
          <div className="space-y-3">
            <div className="flex items-center text-slate-300">
              <Phone className="w-4 h-4 mr-3 text-cyan-400" />
              <span>+213 779 154 202</span>
            </div>
            <div className="flex items-center text-slate-300">
              <Mail className="w-4 h-4 mr-3 text-cyan-400" />
              <span>Available for projects</span>
            </div>
          </div>
        </div>
      </div>

      {/* Footer */}
      <div className="px-6 py-8">
        <div className="text-center">
          <p className="text-slate-400 text-sm">
            © 2024 Mohamed Seddik Bouchelaghem. Built with React Native.
          </p>
        </div>
      </div>
    </div>
  );
};

export default ProfileApp;
