import React, { useState, useEffect, useRef } from 'react';
import { motion, AnimatePresence } from 'motion/react';
import { ChevronLeft, ChevronRight, Search, Menu, X, ArrowRight, Instagram, Twitter, Facebook } from 'lucide-react';

// --- Types ---
interface CarouselImage {
  id: number;
  url: string;
  title: string;
  category: string;
}

const IMAGES: CarouselImage[] = [
  { id: 1, url: 'https://picsum.photos/seed/gush1/1200/800', title: 'Modern Architecture', category: 'Design' },
  { id: 2, url: 'https://picsum.photos/seed/gush2/1200/800', title: 'Minimalist Interior', category: 'Living' },
  { id: 3, url: 'https://picsum.photos/seed/gush3/1200/800', title: 'Urban Landscape', category: 'City' },
  { id: 4, url: 'https://picsum.photos/seed/gush4/1200/800', title: 'Natural Elements', category: 'Nature' },
  { id: 5, url: 'https://picsum.photos/seed/gush5/1200/800', title: 'Abstract Forms', category: 'Art' },
];

export default function App() {
  const [isHeaderSticky, setIsHeaderSticky] = useState(false);
  const [lastScrollY, setLastScrollY] = useState(0);
  const [currentImageIndex, setCurrentImageIndex] = useState(0);
  const [isMenuOpen, setIsMenuOpen] = useState(false);
  const [zoomPos, setZoomPos] = useState({ x: 0, y: 0 });
  const [isZooming, setIsZooming] = useState(false);

  const carouselRef = useRef<HTMLDivElement>(null);

  // --- Sticky Header Logic ---
  useEffect(() => {
    const handleScroll = () => {
      const currentScrollY = window.scrollY;
      const firstFoldHeight = window.innerHeight * 0.8;

      // Sticky header logic: 
      // 1. Appears when scrolling beyond first fold
      // 2. Disappears when scrolling back up
      if (currentScrollY > firstFoldHeight) {
        if (currentScrollY < lastScrollY) {
          // Scrolling UP - show header
          setIsHeaderSticky(true);
        } else {
          // Scrolling DOWN - hide header
          setIsHeaderSticky(false);
        }
      } else {
        setIsHeaderSticky(false);
      }

      setLastScrollY(currentScrollY);
    };

    window.addEventListener('scroll', handleScroll, { passive: true });
    return () => window.removeEventListener('scroll', handleScroll);
  }, [lastScrollY]);

  // --- Carousel Logic ---
  const nextImage = () => {
    setCurrentImageIndex((prev) => (prev + 1) % IMAGES.length);
  };

  const prevImage = () => {
    setCurrentImageIndex((prev) => (prev - 1 + IMAGES.length) % IMAGES.length);
  };

  // --- Zoom Logic ---
  const handleMouseMove = (e: React.MouseEvent<HTMLDivElement>) => {
    if (!carouselRef.current) return;
    const { left, top, width, height } = carouselRef.current.getBoundingClientRect();
    const x = ((e.clientX - left) / width) * 100;
    const y = ((e.clientY - top) / height) * 100;
    setZoomPos({ x, y });
  };

  return (
    <div className="min-h-screen bg-[#444444] selection:bg-white/20">
      {/* --- Navigation Bar (Static) --- */}
      <nav className="relative z-40 border-b border-white/10 bg-[#444444]">
        <div className="container-custom flex items-center justify-between h-20">
          <div className="flex items-center gap-8">
            <a href="#" className="text-2xl font-bold tracking-tighter uppercase">Gushwork</a>
            <div className="hidden md:flex items-center gap-6 text-sm font-medium text-white/60">
              <a href="#" className="hover:text-white transition-colors">Work</a>
              <a href="#" className="hover:text-white transition-colors">Services</a>
              <a href="#" className="hover:text-white transition-colors">About</a>
              <a href="#" className="hover:text-white transition-colors">Contact</a>
            </div>
          </div>
          <div className="flex items-center gap-4">
            <button className="p-2 hover:bg-white/5 rounded-full transition-colors">
              <Search size={20} />
            </button>
            <button 
              className="md:hidden p-2 hover:bg-white/5 rounded-full transition-colors"
              onClick={() => setIsMenuOpen(!isMenuOpen)}
            >
              {isMenuOpen ? <X size={24} /> : <Menu size={24} />}
            </button>
            <button className="hidden md:block px-6 py-2 bg-white text-black text-sm font-bold rounded-full hover:bg-white/90 transition-colors">
              Get Started
            </button>
          </div>
        </div>
      </nav>

      {/* --- Mobile Menu --- */}
      <AnimatePresence>
        {isMenuOpen && (
          <motion.div 
            initial={{ opacity: 0, y: -20 }}
            animate={{ opacity: 1, y: 0 }}
            exit={{ opacity: 0, y: -20 }}
            className="fixed inset-0 z-50 bg-[#444444] pt-24 px-6 md:hidden"
          >
            <div className="flex flex-col gap-8 text-3xl font-bold">
              <a href="#" onClick={() => setIsMenuOpen(false)}>Work</a>
              <a href="#" onClick={() => setIsMenuOpen(false)}>Services</a>
              <a href="#" onClick={() => setIsMenuOpen(false)}>About</a>
              <a href="#" onClick={() => setIsMenuOpen(false)}>Contact</a>
            </div>
          </motion.div>
        )}
      </AnimatePresence>

      {/* --- Sticky Header --- */}
      <motion.header 
        initial={{ y: -100 }}
        animate={{ y: isHeaderSticky ? 0 : -100 }}
        transition={{ type: 'spring', damping: 25, stiffness: 200 }}
        className="fixed top-0 left-0 right-0 z-50 bg-[#444444]/80 backdrop-blur-md border-b border-white/10"
      >
        <div className="container-custom flex items-center justify-between h-16">
          <a href="#" className="text-xl font-bold tracking-tighter uppercase">Gushwork</a>
          <div className="flex items-center gap-6">
            <div className="hidden sm:flex items-center gap-4 text-xs font-bold uppercase tracking-widest text-white/60">
              <a href="#" className="hover:text-white transition-colors">Portfolio</a>
              <a href="#" className="hover:text-white transition-colors">Inquiry</a>
            </div>
            <button className="px-4 py-1.5 bg-white text-black text-xs font-bold rounded-full hover:bg-white/90 transition-colors">
              Contact
            </button>
          </div>
        </div>
      </motion.header>

      {/* --- Hero Section --- */}
      <section className="relative pt-20 pb-32 overflow-hidden">
        <div className="container-custom">
          <div className="grid lg:grid-cols-2 gap-16 items-center">
            <motion.div
              initial={{ opacity: 0, x: -50 }}
              whileInView={{ opacity: 1, x: 0 }}
              viewport={{ once: true }}
              transition={{ duration: 0.8 }}
            >
              <span className="inline-block px-3 py-1 bg-white/10 rounded-full text-[10px] font-bold uppercase tracking-[0.2em] mb-6">
                Creative Studio
              </span>
              <h1 className="text-6xl md:text-8xl font-bold leading-[0.9] tracking-tighter mb-8">
                CRAFTING <br />
                <span className="text-white/40 italic">DIGITAL</span> <br />
                EXCELLENCE
              </h1>
              <p className="text-lg text-white/60 max-w-md mb-10 leading-relaxed">
                We bridge the gap between imagination and reality through meticulous design and cutting-edge technology.
              </p>
              <div className="flex flex-wrap gap-4">
                <button className="group flex items-center gap-2 px-8 py-4 bg-white text-black font-bold rounded-full hover:scale-105 transition-transform">
                  View Projects <ArrowRight size={18} className="group-hover:translate-x-1 transition-transform" />
                </button>
                <button className="px-8 py-4 border border-white/20 font-bold rounded-full hover:bg-white/5 transition-colors">
                  Our Story
                </button>
              </div>
            </motion.div>

            <motion.div
              initial={{ opacity: 0, scale: 0.9 }}
              whileInView={{ opacity: 1, scale: 1 }}
              viewport={{ once: true }}
              transition={{ duration: 1 }}
              className="relative aspect-square rounded-2xl overflow-hidden border border-white/10"
            >
              <img 
                src="https://picsum.photos/seed/hero/1000/1000" 
                alt="Hero" 
                className="w-full h-full object-cover"
                referrerPolicy="no-referrer"
              />
              <div className="absolute inset-0 bg-gradient-to-t from-black/60 to-transparent" />
              <div className="absolute bottom-8 left-8">
                <p className="text-sm font-bold uppercase tracking-widest text-white/60 mb-2">Featured Work</p>
                <h3 className="text-2xl font-bold">The Zenith Collection</h3>
              </div>
            </motion.div>
          </div>
        </div>
      </section>

      {/* --- Image Carousel with Zoom --- */}
      <section className="py-32 bg-black/20">
        <div className="container-custom">
          <div className="flex items-end justify-between mb-12">
            <div>
              <h2 className="text-4xl font-bold tracking-tight mb-4">Gallery Showcase</h2>
              <p className="text-white/40 max-w-sm">Explore our latest visual explorations and design prototypes.</p>
            </div>
            <div className="flex gap-4">
              <button 
                onClick={prevImage}
                className="p-4 border border-white/10 rounded-full hover:bg-white hover:text-black transition-all"
              >
                <ChevronLeft size={24} />
              </button>
              <button 
                onClick={nextImage}
                className="p-4 border border-white/10 rounded-full hover:bg-white hover:text-black transition-all"
              >
                <ChevronRight size={24} />
              </button>
            </div>
          </div>

          <div className="relative group">
            <div 
              ref={carouselRef}
              className="relative aspect-[16/9] md:aspect-[21/9] rounded-3xl overflow-hidden border border-white/10 cursor-zoom-in"
              onMouseMove={handleMouseMove}
              onMouseEnter={() => setIsZooming(true)}
              onMouseLeave={() => setIsZooming(false)}
            >
              <AnimatePresence mode="wait">
                <motion.div
                  key={currentImageIndex}
                  initial={{ opacity: 0 }}
                  animate={{ opacity: 1 }}
                  exit={{ opacity: 0 }}
                  transition={{ duration: 0.5 }}
                  className="w-full h-full"
                >
                  <img 
                    src={IMAGES[currentImageIndex].url} 
                    alt={IMAGES[currentImageIndex].title}
                    className="w-full h-full object-cover transition-transform duration-700"
                    style={{
                      transform: isZooming ? `scale(1.5)` : 'scale(1)',
                      transformOrigin: `${zoomPos.x}% ${zoomPos.y}%`
                    }}
                    referrerPolicy="no-referrer"
                  />
                </motion.div>
              </AnimatePresence>

              {/* Overlay Info */}
              <div className="absolute bottom-0 left-0 right-0 p-8 md:p-12 bg-gradient-to-t from-black/80 via-black/20 to-transparent pointer-events-none">
                <motion.div
                  key={currentImageIndex}
                  initial={{ y: 20, opacity: 0 }}
                  animate={{ y: 0, opacity: 1 }}
                  transition={{ delay: 0.2 }}
                >
                  <span className="text-xs font-bold uppercase tracking-[0.3em] text-white/60 mb-2 block">
                    {IMAGES[currentImageIndex].category}
                  </span>
                  <h3 className="text-3xl md:text-5xl font-bold tracking-tighter">
                    {IMAGES[currentImageIndex].title}
                  </h3>
                </motion.div>
              </div>

              {/* Zoom Indicator */}
              {!isZooming && (
                <div className="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 opacity-0 group-hover:opacity-100 transition-opacity pointer-events-none">
                  <div className="bg-white/20 backdrop-blur-md px-6 py-3 rounded-full border border-white/20 text-xs font-bold uppercase tracking-widest">
                    Hover to Zoom
                  </div>
                </div>
              )}
            </div>

            {/* Thumbnails */}
            <div className="flex gap-4 mt-8 overflow-x-auto pb-4 no-scrollbar">
              {IMAGES.map((img, idx) => (
                <button
                  key={img.id}
                  onClick={() => setCurrentImageIndex(idx)}
                  className={`relative flex-shrink-0 w-32 aspect-video rounded-lg overflow-hidden border-2 transition-all ${
                    currentImageIndex === idx ? 'border-white scale-105' : 'border-transparent opacity-40 hover:opacity-100'
                  }`}
                >
                  <img src={img.url} alt={img.title} className="w-full h-full object-cover" referrerPolicy="no-referrer" />
                </button>
              ))}
            </div>
          </div>
        </div>
      </section>

      {/* --- Features Grid --- */}
      <section className="py-32">
        <div className="container-custom">
          <div className="grid md:grid-cols-3 gap-1px bg-white/10 border border-white/10 rounded-3xl overflow-hidden">
            {[
              { title: 'Strategy', desc: 'Defining the path to success through data-driven insights and market analysis.' },
              { title: 'Design', desc: 'Creating visual languages that resonate with your audience and elevate your brand.' },
              { title: 'Technology', desc: 'Building robust, scalable solutions using the latest frameworks and tools.' }
            ].map((feature, i) => (
              <div key={i} className="bg-[#444444] p-12 hover:bg-white/5 transition-colors group">
                <span className="text-white/20 text-4xl font-bold mb-8 block group-hover:text-white/40 transition-colors">0{i + 1}</span>
                <h4 className="text-2xl font-bold mb-4">{feature.title}</h4>
                <p className="text-white/60 leading-relaxed">{feature.desc}</p>
              </div>
            ))}
          </div>
        </div>
      </section>

      {/* --- Footer --- */}
      <footer className="bg-black py-24 border-t border-white/10">
        <div className="container-custom">
          <div className="grid md:grid-cols-2 lg:grid-cols-4 gap-12 mb-20">
            <div className="lg:col-span-2">
              <a href="#" className="text-3xl font-bold tracking-tighter uppercase mb-8 block">Gushwork</a>
              <p className="text-white/40 max-w-sm mb-8">
                A global creative studio dedicated to building the future of digital interaction.
              </p>
              <div className="flex gap-4">
                <a href="#" className="p-3 border border-white/10 rounded-full hover:bg-white hover:text-black transition-all">
                  <Instagram size={20} />
                </a>
                <a href="#" className="p-3 border border-white/10 rounded-full hover:bg-white hover:text-black transition-all">
                  <Twitter size={20} />
                </a>
                <a href="#" className="p-3 border border-white/10 rounded-full hover:bg-white hover:text-black transition-all">
                  <Facebook size={20} />
                </a>
              </div>
            </div>
            <div>
              <h5 className="font-bold uppercase tracking-widest text-xs mb-8">Company</h5>
              <ul className="space-y-4 text-white/60 text-sm">
                <li><a href="#" className="hover:text-white transition-colors">About Us</a></li>
                <li><a href="#" className="hover:text-white transition-colors">Careers</a></li>
                <li><a href="#" className="hover:text-white transition-colors">Press</a></li>
                <li><a href="#" className="hover:text-white transition-colors">Contact</a></li>
              </ul>
            </div>
            <div>
              <h5 className="font-bold uppercase tracking-widest text-xs mb-8">Newsletter</h5>
              <p className="text-white/40 text-sm mb-6">Stay updated with our latest news and insights.</p>
              <div className="flex gap-2">
                <input 
                  type="email" 
                  placeholder="Email address" 
                  className="bg-white/5 border border-white/10 rounded-full px-4 py-2 text-sm focus:outline-none focus:border-white/40 flex-grow"
                />
                <button className="bg-white text-black p-2 rounded-full hover:bg-white/90 transition-colors">
                  <ArrowRight size={18} />
                </button>
              </div>
            </div>
          </div>
          <div className="pt-12 border-t border-white/10 flex flex-col md:flex-row justify-between gap-6 text-[10px] font-bold uppercase tracking-widest text-white/20">
            <p>© 2026 Gushwork Studio. All rights reserved.</p>
            <div className="flex gap-8">
              <a href="#" className="hover:text-white transition-colors">Privacy Policy</a>
              <a href="#" className="hover:text-white transition-colors">Terms of Service</a>
            </div>
          </div>
        </div>
      </footer>
    </div>
  );
}
