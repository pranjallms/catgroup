import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { motion } from "framer-motion";
import { FaLaptop, FaMobileAlt, FaGlobe } from "react-icons/fa";

const services = [
  { icon: <FaLaptop size={40} />, title: "Web Development", desc: "Professional and modern websites tailored to your needs." },
  { icon: <FaMobileAlt size={40} />, title: "App Development", desc: "Mobile applications that provide seamless user experience." },
  { icon: <FaGlobe size={40} />, title: "SEO & Digital Marketing", desc: "Optimizing your online presence for better reach and growth." },
];

const Home = () => {
  return (
    <div className="bg-gray-100 min-h-screen text-gray-900">
      {/* Header Section */}
      <header className="bg-blue-600 text-white p-6 text-center text-3xl font-bold">
        Welcome to The Cat Group
      </header>

      {/* Hero Section */}
      <section className="flex flex-col md:flex-row items-center justify-center py-16 px-6">
        <motion.div initial={{ opacity: 0, y: -20 }} animate={{ opacity: 1, y: 0 }} className="max-w-lg text-center md:text-left">
          <h1 className="text-4xl font-extrabold">Your Digital Partner</h1>
          <p className="text-lg mt-4">We provide top-notch IT solutions to help you grow your business.</p>
          <Button className="mt-6">Get Started</Button>
        </motion.div>
      </section>

      {/* Services Section */}
      <section className="py-16 bg-white text-center">
        <h2 className="text-3xl font-bold">Our Services</h2>
        <div className="grid grid-cols-1 md:grid-cols-3 gap-8 mt-8 px-6">
          {services.map((service, index) => (
            <Card key={index} className="p-6 shadow-lg rounded-lg hover:shadow-2xl transition">
              <CardContent className="flex flex-col items-center">
                <div className="text-blue-600">{service.icon}</div>
                <h3 className="text-xl font-bold mt-4">{service.title}</h3>
                <p className="mt-2">{service.desc}</p>
              </CardContent>
            </Card>
          ))}
        </div>
      </section>

      {/* Footer */}
      <footer className="bg-gray-900 text-white text-center p-4">
        &copy; 2025 The Cat Group | All Rights Reserved
      </footer>
    </div>
  );
};

export default Home;
