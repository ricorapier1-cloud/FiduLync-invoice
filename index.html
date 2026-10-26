import React, { useState, useEffect } from 'react';
import { 
  ShoppingBag, 
  Settings, 
  Plus, 
  Trash2, 
  Send, 
  DollarSign, 
  TrendingUp, 
  FileText, 
  CheckCircle, 
  Search, 
  ExternalLink,
  ShieldCheck,
  Smartphone,
  Tag,
  Percent,
  Truck,
  Download,
  Store,
  CreditCard,
  User,
  ArrowRight
} from 'lucide-react';

export default function App() {
  // Navigation & View Mode
  const [activeTab, setActiveTab] = useState('buyer'); // 'buyer' or 'admin'
  const [currency, setCurrency] = useState('NGN'); // 'NGN', 'USD', 'GBP', 'EUR'
  const [searchTerm, setSearchTerm] = useState('');
  const [selectedCategory, setSelectedCategory] = useState('All');

  // Merchant Settings State
  const [merchant, setMerchant] = useState({
    businessName: 'Luxe Attire Hub',
    tagline: 'Premium Afro-Centric Couture & Accessories',
    whatsapp: '+2348031234567',
    bankName: 'United Bank for Africa (UBA)',
    accountNumber: '2089858929',
    accountName: 'Akinsooto Eric',
    taxRate: 7.5,
    shippingFee: 2000,
    subscriptionPlan: 'Pro Growth (₦5,000/mo)'
  });

  // Product Catalog State
  const [products, setProducts] = useState([
    {
      id: 1,
      name: 'Ankara Multi-Wear Maxi Dress',
      category: 'Apparel',
      priceNGN: 28500,
      image: 'https://images.unsplash.com/photo-1584273143981-41c073dfe8f8?auto=format&fit=crop&w=600&q=80',
      sku: 'LUX-ANK-001',
      stock: 6,
      variants: ['Small / Red', 'Medium / Blue', 'Large / Gold'],
      description: 'Handmade 100% African wax print dress with a convertible neckline and side pockets.'
    },
    {
      id: 2,
      name: 'Handcrafted Bead Handbag',
      category: 'Accessories',
      priceNGN: 18000,
      image: 'https://images.unsplash.com/photo-1590874103328-eac38a683ce7?auto=format&fit=crop&w=600&q=80',
      sku: 'LUX-BDG-002',
      stock: 12,
      variants: ['Emerald Green', 'Royal Blue', 'Sunset Gold'],
      description: 'Artisan Lagos handcrafted luxury crystal beaded shoulder bag with detachable chain.'
    },
    {
      id: 3,
      name: 'Executive Agbada Set',
      category: 'Men Wear',
      priceNGN: 65000,
      image: 'https://images.unsplash.com/photo-1617137984095-74e4e5e3613f?auto=format&fit=crop&w=600&q=80',
      sku: 'LUX-AGB-003',
      stock: 4,
      variants: ['Standard / Navy Blue', 'Tall / Charcoal Grey'],
      description: 'Premium tailored traditional Agbada with intricate chest embroidery and matching trousers.'
    },
    {
      id: 4,
      name: 'Leather Slide Sandals',
      category: 'Footwear',
      profile: 'Footwear',
      priceNGN: 15000,
      image: 'https://images.unsplash.com/photo-1603808033192-082d6939d3e1?auto=format&fit=crop&w=600&q=80',
      sku: 'LUX-SND-004',
      stock: 9,
      variants: ['Size 40 / Tan', 'Size 42 / Dark Brown', 'Size 44 / Black'],
      description: 'Genuine cowhide leather slides crafted for durability and everyday street comfort.'
    }
  ]);

  // Shopping Cart State
  const [cart, setCart] = useState([]);
  
  // Checkout Metadata State
  const [customer, setCustomer] = useState({
    name: 'Akin Ola',
    phone: '08031234567',
    address: '15 Admiralty Way, Lekki Phase 1, Lagos',
    region: 'Lagos Mainland/Island',
    discountType: 'percentage', // 'percentage' or 'fixed'
    discountValue: 0,
    paymentMethod: 'Bank Transfer'
  });

  // Orders Archive State
  const [orders, setOrders] = useState([
    {
      id: 'INV-20261026-01',
      date: '2026-10-26 14:32',
      customerName: 'Tunde Bakare',
      phone: '+2348011223344',
      items: [{ name: 'Ankara Multi-Wear Maxi Dress', qty: 1, price: 28500 }],
      total: 32675,
      status: 'Paid',
      paymentRef: 'PAYSTACK-NGN-98234'
    },
    {
      id: 'INV-20261026-02',
      date: '2026-10-26 18:05',
      customerName: 'Chidinma Okeke',
      phone: '+2348099887766',
      items: [{ name: 'Handcrafted Bead Handbag', qty: 2, price: 18000 }],
      total: 41350,
      status: 'Pending',
      paymentRef: 'Bank Transfer'
    }
  ]);

  // Currency Converter Multiplier
  const rates = { NGN: 1, USD: 0.00065, GBP: 0.00050, EUR: 0.00060 };
  const symbols = { NGN: '₦', USD: '$', GBP: '£', EUR: '€' };

  const formatPrice = (amountInNGN) => {
    const converted = amountInNGN * rates[currency];
    return `${symbols[currency]}${converted.toLocaleString(undefined, { minimumFractionDigits: 0, maximumFractionDigits: 2 })}`;
  };

  // Cart Handlers
  const addToCart = (product, selectedVariant) => {
    const existingIndex = cart.findIndex(item => item.id === product.id && item.variant === selectedVariant);
    if (existingIndex > -1) {
      const updated = [...cart];
      updated[existingIndex].qty += 1;
      setCart(updated);
    } else {
      setCart([...cart, {
        id: product.id,
        name: product.name,
        price: product.priceNGN,
        variant: selectedVariant || 'Standard',
        qty: 1
      }]);
    }
  };

  const updateCartQty = (index, delta) => {
    const updated = [...cart];
    updated[index].qty += delta;
    if (updated[index].qty <= 0) {
      updated.splice(index, 1);
    }
    setCart(updated);
  };

  // Financial Calculations
  const subtotal = cart.reduce((acc, item) => acc + (item.price * item.qty), 0);
  
  const discountAmount = customer.discountType === 'percentage' 
    ? (subtotal * (customer.discountValue || 0)) / 100 
    : (customer.discountValue || 0);

  const taxableAmount = Math.max(0, subtotal - discountAmount);
  const taxAmount = (taxableAmount * merchant.taxRate) / 100;
  const shippingCost = merchant.shippingFee;
  const grandTotal = taxableAmount + taxAmount + shippingCost;

  // Generate WhatsApp Payload
  const generateWhatsAppMessage = () => {
    const refId = `INV-${Date.now().toString().slice(-6)}`;
    const itemsList = cart.map((item, i) => `${i + 1}. *${item.name}* (${item.variant}) - ${item.qty}x @ ${formatPrice(item.price)}`).join('\n');
    
    const message = `*INVOICE #${refId}*
📅 *Date:* ${new Date().toLocaleDateString()}
👤 *Client:* ${customer.name}
📍 *Delivery Address:* ${customer.address}

----------------------------------
*ORDERED ITEMS:*
${itemsList}
----------------------------------
Subtotal: ${formatPrice(subtotal)}
${discountAmount > 0 ? `Discount: -${formatPrice(discountAmount)}\n` : ''}VAT (${merchant.taxRate}%): +${formatPrice(taxAmount)}
Shipping (${customer.region}): +${formatPrice(shippingCost)}
----------------------------------
*GRAND TOTAL DUE: ${formatPrice(grandTotal)}*
----------------------------------

💳 *Payment Instructions:*
Bank: ${merchant.bankName}
Account Number: ${merchant.accountNumber}
Account Name: ${merchant.accountName}

*(Please reply with your payment receipt once transferred).*
Thank you for shopping with *${merchant.businessName}*!`;

    const encoded = encodeURIComponent(message);
    const cleanPhone = merchant.whatsapp.replace(/[^0-9]/g, '');
    const waUrl = `https://wa.me/${cleanPhone}?text=${encoded}`;
    
    // Save to orders archive
    setOrders([{
      id: refId,
      date: new Date().toISOString().replace('T', ' ').substring(0, 16),
      customerName: customer.name,
      phone: customer.phone,
      items: [...cart],
      total: grandTotal,
      status: 'Pending',
      paymentRef: customer.paymentMethod
    }, ...orders]);

    window.open(waUrl, '_blank');
  };

  return (
    <div className="min-h-screen bg-slate-950 text-slate-100 font-sans pb-16">
      {/* Top Header Navigation */}
      <header className="border-b border-slate-800 bg-slate-900/80 backdrop-blur sticky top-0 z-50 px-4 py-3 flex items-center justify-between">
        <div className="flex items-center space-x-3">
          <div className="bg-gradient-to-tr from-emerald-500 to-teal-400 p-2 rounded-xl text-slate-950 font-black shadow-lg shadow-emerald-500/20">
            <Store className="w-5 h-5" />
          </div>
          <div>
            <h1 className="font-bold text-lg tracking-tight flex items-center gap-2">
              {merchant.businessName}
              <span className="text-[10px] bg-emerald-500/20 text-emerald-400 px-2 py-0.5 rounded-full border border-emerald-500/30">Enterprise v3.4</span>
            </h1>
            <p className="text-xs text-slate-400">Secure WhatsApp Checkout & Invoicing Suite</p>
          </div>
        </div>

        <div className="flex items-center space-x-2">
          {/* Currency Switcher */}
          <select 
            value={currency} 
            onChange={(e) => setCurrency(e.target.value)}
            className="bg-slate-800 border border-slate-700 text-xs px-2.5 py-1.5 rounded-lg font-medium text-slate-200 focus:outline-none focus:border-emerald-500"
          >
            <option value="NGN">NGN (₦)</option>
            <option value="USD">USD ($)</option>
            <option value="GBP">GBP (£)</option>
            <option value="EUR">EUR (€)</option>
          </select>

          {/* View Toggles */}
          <button 
            onClick={() => setActiveTab('buyer')}
            className={`px-3 py-1.5 rounded-lg text-xs font-semibold transition flex items-center gap-1.5 ${activeTab === 'buyer' ? 'bg-emerald-500 text-slate-950 shadow-md shadow-emerald-500/30' : 'bg-slate-800 text-slate-300 hover:bg-slate-700'}`}
          >
            <ShoppingBag className="w-3.5 h-3.5" /> Buyer Store
          </button>
          <button 
            onClick={() => setActiveTab('admin')}
            className={`px-3 py-1.5 rounded-lg text-xs font-semibold transition flex items-center gap-1.5 ${activeTab === 'admin' ? 'bg-emerald-500 text-slate-950 shadow-md shadow-emerald-500/30' : 'bg-slate-800 text-slate-300 hover:bg-slate-700'}`}
          >
            <Settings className="w-3.5 h-3.5" /> Vendor Admin
          </button>
        </div>
      </header>

      {/* Main Container */}
      <main className="max-w-7xl mx-auto px-4 py-6">
        {activeTab === 'buyer' ? (
          <div className="grid grid-cols-1 lg:grid-cols-12 gap-6">
            
            {/* Left Column: Store Catalog */}
            <div className="lg:col-span-7 space-y-4">
              {/* Vendor Banner Card */}
              <div className="bg-gradient-to-r from-slate-900 via-slate-900 to-emerald-950/40 border border-slate-800 rounded-2xl p-5 shadow-xl relative overflow-hidden">
                <div className="absolute right-4 top-4 bg-emerald-500/10 border border-emerald-500/20 text-emerald-400 px-3 py-1 rounded-full text-xs font-medium flex items-center gap-1">
                  <ShieldCheck className="w-3.5 h-3.5" /> Official Vendor
                </div>
                <h2 className="text-xl font-bold text-white mb-1">{merchant.businessName}</h2>
                <p className="text-sm text-slate-400 mb-3">{merchant.tagline}</p>
                <div className="flex flex-wrap gap-4 text-xs text-slate-300">
                  <span className="flex items-center gap-1"><Instagram className="w-3.5 h-3.5 text-pink-400" /> @luxeattire_ng</span>
                  <span className="flex items-center gap-1"><Send className="w-3.5 h-3.5 text-emerald-400" /> Direct WhatsApp: {merchant.whatsapp}</span>
                </div>
              </div>

              {/* Search & Categories */}
              <div className="flex flex-col sm:flex-row gap-3">
                <div className="relative flex-1">
                  <Search className="absolute left-3.5 top-3 w-4 h-4 text-slate-400" />
                  <input 
                    type="text"
                    placeholder="Search products or descriptions..."
                    value={searchTerm}
                    onChange={(e) => setSearchTerm(e.target.value)}
                    className="w-full bg-slate-900 border border-slate-800 rounded-xl pl-10 pr-4 py-2.5 text-sm text-slate-200 placeholder-slate-500 focus:outline-none focus:border-emerald-500"
                  />
                </div>
                <div className="flex gap-1.5 overflow-x-auto pb-1">
                  {['All', 'Apparel', 'Accessories', 'Men Wear', 'Footwear'].map((cat) => (
                    <button
                      key={cat}
                      onClick={() => setSelectedCategory(cat)}
                      className={`px-3 py-2 rounded-xl text-xs font-medium whitespace-nowrap transition ${selectedCategory === cat ? 'bg-emerald-500 text-slate-950 font-bold' : 'bg-slate-900 border border-slate-800 text-slate-400 hover:text-white'}`}
                    >
                      {cat}
                    </button>
                  ))}
                </div>
              </div>

              {/* Product Grid */}
              <div className="grid grid-cols-1 sm:grid-cols-2 gap-4">
                {products
                  .filter(p => selectedCategory === 'All' || p.category === selectedCategory)
                  .filter(p => p.name.toLowerCase().includes(searchTerm.toLowerCase()))
                  .map((product) => {
                    const [selectedVariant, setSelectedVariant] = useState(product.variants[0]);
                    return (
                      <div key={product.id} className="bg-slate-900 border border-slate-800 rounded-2xl overflow-hidden shadow-lg flex flex-col justify-between group hover:border-slate-700 transition">
                        <div>
                          <div className="relative h-48 overflow-hidden bg-slate-950">
                            <img src={product.image} alt={product.name} className="w-full h-full object-cover group-hover:scale-105 transition duration-300" />
                            <span className="absolute top-2.5 left-2.5 bg-slate-950/80 backdrop-blur border border-slate-800 text-[10px] px-2.5 py-1 rounded-full text-slate-300 font-medium">
                              {product.category}
                            </span>
                          </div>
                          <div className="p-4">
                            <div className="flex justify-between items-start mb-1">
                              <h3 className="font-semibold text-sm text-slate-100">{product.name}</h3>
                              <span className="text-[10px] text-slate-500 font-mono">{product.sku}</span>
                            </div>
                            <p className="text-xs text-slate-400 line-clamp-2 mb-3">{product.description}</p>
                            
                            {/* Variant Selector */}
                            <div className="mb-3">
                              <label className="text-[10px] uppercase font-bold text-slate-500 block mb-1">Select Option / Variant</label>
                              <select 
                                value={selectedVariant}
                                onChange={(e) => setSelectedVariant(e.target.value)}
                                className="w-full bg-slate-950 border border-slate-800 rounded-lg px-2.5 py-1.5 text-xs text-slate-300 focus:outline-none focus:border-emerald-500"
                              >
                                {product.variants.map(v => (
                                  <option key={v} value={v}>{v}</option>
                                ))}
                              </select>
                            </div>
                          </div>
                        </div>

                        <div className="p-4 pt-0 flex items-center justify-between
