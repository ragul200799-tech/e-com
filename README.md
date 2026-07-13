# Premium E-Commerce Website

A full-stack e-commerce platform with modern UI/UX similar to Amazon, Flipkart, and Apple Store. Built with Node.js, Express, MongoDB, and vanilla JavaScript.

## 🚀 Features

### User Features
- ✅ User registration/login with JWT authentication
- ✅ Email verification
- ✅ Profile management with profile picture upload
- ✅ Advanced product search with live suggestions
- ✅ Filter by category, price range, brand, and ratings
- ✅ Sort products by popularity, price, ratings
- ✅ Wishlist management
- ✅ Shopping cart with quantity updates
- ✅ Coupon code application
- ✅ Secure checkout with multiple payment options
- ✅ Cash on Delivery (COD)
- ✅ Razorpay payment integration
- ✅ Order tracking and history
- ✅ Product reviews and ratings
- ✅ Recently viewed products
- ✅ Recommended products
- ✅ Real-time notifications

### Admin Features
- ✅ Secure admin dashboard
- ✅ Analytics and sales reports
- ✅ Product management (CRUD)
- ✅ Category and brand management
- ✅ Inventory management
- ✅ Multiple product image uploads
- ✅ User management
- ✅ Order management with status updates
- ✅ Coupon management
- ✅ Revenue charts and metrics
- ✅ Review moderation

### UI/UX Features
- ✅ Modern responsive design
- ✅ Glassmorphism + soft shadows
- ✅ Dark/Light mode toggle
- ✅ Smooth animations
- ✅ Mobile-first layout
- ✅ Professional typography
- ✅ Loading animations & skeletons
- ✅ Sticky navigation
- ✅ Gradient buttons
- ✅ High-quality product cards
- ✅ Multi-image product gallery with zoom
- ✅ Breadcrumb navigation
- ✅ Lazy loading images
- ✅ Pagination & infinite scrolling

## 📋 Tech Stack

### Frontend
- HTML5
- CSS3 (Glassmorphism, Gradients, Animations)
- JavaScript ES6+
- Fetch API
- LocalStorage for state management

### Backend
- Node.js
- Express.js
- MongoDB with Mongoose
- JWT (jsonwebtoken)
- bcryptjs for password hashing
- Multer for file uploads
- Nodemailer for email notifications
- Razorpay API integration

### Database
- MongoDB
- Collections: Users, Products, Categories, Orders, Cart, Wishlist, Reviews, Coupons, Payments, Notifications

## 📁 Project Structure

```
e-com/
├── client/
│   ├── assets/
│   │   ├── icons/
│   │   └── images/
│   ├── css/
│   │   ├── styles.css
│   │   ├── responsive.css
│   │   ├── animations.css
│   │   └── variables.css
│   ├── js/
│   │   ├── api.js
│   │   ├── auth.js
│   │   ├── cart.js
│   │   ├── wishlist.js
│   │   ├── product.js
│   │   ├── utils.js
│   │   └── theme.js
│   └── pages/
│       ├── index.html
│       ├── shop.html
│       ├── product.html
│       ├── categories.html
│       ├── cart.html
│       ├── checkout.html
│       ├── order-success.html
│       ├── wishlist.html
│       ├── login.html
│       ├── register.html
│       ├── forgot-password.html
│       ├── dashboard.html
│       ├── admin-dashboard.html
│       ├── about.html
│       ├── contact.html
│       └── 404.html
├── server/
│   ├── config/
│   │   └── db.js
│   ├── controllers/
│   │   ├── authController.js
│   │   ├── productController.js
│   │   ├── categoryController.js
│   │   ├── cartController.js
│   │   ├── wishlistController.js
│   │   ├── orderController.js
│   │   ├── paymentController.js
│   │   ├── reviewController.js
│   │   ├── couponController.js
│   │   ├── userController.js
│   │   ├── adminController.js
│   │   └── notificationController.js
│   ├── middleware/
│   │   ├── auth.js
│   │   ├── errorHandler.js
│   │   ├── validation.js
│   │   └── upload.js
│   ├── models/
│   │   ├── User.js
│   │   ├── Product.js
│   │   ├── Category.js
│   │   ├── Order.js
│   │   ├── Cart.js
│   │   ├── Wishlist.js
│   │   ├── Review.js
│   │   ├── Coupon.js
│   │   ├── Payment.js
│   │   └── Notification.js
│   ├── routes/
│   │   ├── auth.js
│   │   ├── products.js
│   │   ├── categories.js
│   │   ├── cart.js
│   │   ├── wishlist.js
│   │   ├── orders.js
│   │   ├── payments.js
│   │   ├── reviews.js
│   │   ├── coupons.js
│   │   ├── users.js
│   │   ├── admin.js
│   │   └── notifications.js
│   ├── utils/
│   │   ├── emailService.js
│   │   ├── jwtUtils.js
│   │   ├── validators.js
│   │   └── helpers.js
│   ├── uploads/
│   ├── app.js
│   ├── server.js
│   └── seeds.js
├── .env.example
├── .gitignore
├── package.json
└── README.md
```

## 🔧 Installation

### Prerequisites
- Node.js (v14 or higher)
- MongoDB (local or Atlas)
- npm or yarn

### Setup Instructions

1. **Clone the repository**
```bash
git clone https://github.com/ragul200799-tech/e-com.git
cd e-com
```

2. **Install dependencies**
```bash
npm install
```

3. **Configure environment variables**
```bash
cp .env.example .env
```
Update `.env` with your configuration:
```
MONGODB_URI=mongodb://localhost:27017/ecommerce
JWT_SECRET=your_jwt_secret_key
JWT_EXPIRE=7d
ADMIN_EMAIL=admin@example.com
ADMIN_PASSWORD=admin123
RAZORPAY_KEY_ID=your_razorpay_key
RAZORPAY_KEY_SECRET=your_razorpay_secret
EMAIL_USER=your_email@gmail.com
EMAIL_PASSWORD=your_app_password
PORT=5000
NODE_ENV=development
```

4. **Seed database (optional)**
```bash
npm run seed
```

5. **Start the server**
```bash
npm start
```
The application will run at `http://localhost:5000`

## 📚 API Documentation

### Authentication Endpoints
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `POST /api/auth/logout` - User logout
- `POST /api/auth/refresh-token` - Refresh JWT token
- `POST /api/auth/verify-email` - Email verification
- `POST /api/auth/forgot-password` - Initiate password reset
- `POST /api/auth/reset-password` - Reset password

### Product Endpoints
- `GET /api/products` - Get all products (with filters, sorting, pagination)
- `GET /api/products/:id` - Get product details
- `POST /api/products` - Create product (Admin only)
- `PUT /api/products/:id` - Update product (Admin only)
- `DELETE /api/products/:id` - Delete product (Admin only)
- `GET /api/products/search?q=query` - Search products
- `GET /api/categories` - Get all categories
- `POST /api/categories` - Create category (Admin only)

### Cart Endpoints
- `GET /api/cart` - Get user's cart
- `POST /api/cart/add` - Add item to cart
- `PUT /api/cart/update/:itemId` - Update cart item
- `DELETE /api/cart/remove/:itemId` - Remove item from cart
- `DELETE /api/cart/clear` - Clear entire cart

### Wishlist Endpoints
- `GET /api/wishlist` - Get user's wishlist
- `POST /api/wishlist/add/:productId` - Add to wishlist
- `DELETE /api/wishlist/remove/:productId` - Remove from wishlist

### Order Endpoints
- `POST /api/orders` - Create order
- `GET /api/orders` - Get user's orders
- `GET /api/orders/:id` - Get order details
- `PUT /api/orders/:id/cancel` - Cancel order
- `GET /api/orders/:id/invoice` - Download invoice (PDF)

### Payment Endpoints
- `POST /api/payments/razorpay/create` - Create Razorpay order
- `POST /api/payments/razorpay/verify` - Verify Razorpay payment

### Review Endpoints
- `POST /api/reviews/:productId` - Add review
- `GET /api/reviews/:productId` - Get product reviews
- `PUT /api/reviews/:reviewId` - Update review
- `DELETE /api/reviews/:reviewId` - Delete review

### Admin Endpoints
- `GET /api/admin/dashboard` - Dashboard analytics
- `GET /api/admin/orders` - Manage orders
- `PUT /api/admin/orders/:id/status` - Update order status
- `GET /api/admin/users` - Manage users
- `GET /api/admin/reports` - Sales reports

## 🔒 Security Features

- ✅ JWT authentication with token expiration
- ✅ Password hashing with bcryptjs
- ✅ XSS protection
- ✅ CSRF protection
- ✅ Rate limiting on sensitive endpoints
- ✅ Secure HTTP-only cookies
- ✅ Role-based authorization
- ✅ Input validation and sanitization
- ✅ SQL injection prevention via Mongoose
- ✅ Environment variable protection

## 🎨 UI/UX Highlights

- **Glassmorphism Design**: Modern frosted glass effect with backdrop blur
- **Dark/Light Mode**: Toggle theme with persistent storage
- **Responsive**: Mobile-first approach with breakpoints for all devices
- **Animations**: Smooth transitions and loading states
- **Accessibility**: Semantic HTML, ARIA labels, keyboard navigation
- **Performance**: Lazy loading, image optimization, code splitting
- **Typography**: Professional font hierarchy with Google Fonts
- **Color Scheme**: Modern gradient backgrounds and color palette

## 📱 Responsive Breakpoints

- **Mobile**: 320px - 480px
- **Tablet**: 481px - 768px
- **Desktop**: 769px - 1024px
- **Large Desktop**: 1025px+

## 🚀 Deployment

### Deploy to Heroku
```bash
heroku create your-app-name
git push heroku main
```

### Deploy to Vercel (Frontend)
```bash
vercel deploy
```

### Deploy to AWS/DigitalOcean
Follow official deployment guides for Node.js applications.

## 🧪 Testing

```bash
npm test
```

## 📝 Environment Variables

See `.env.example` for complete list of required environment variables.

## 🤝 Contributing

1. Fork the repository
2. Create feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open Pull Request

## 📄 License

This project is licensed under the MIT License - see LICENSE file for details.

## 👨‍💻 Author

**Ragul**
- GitHub: [@ragul200799-tech](https://github.com/ragul200799-tech)

## 📞 Support

For support, email support@ecommerce.com or open an issue on GitHub.

## 🎯 Future Enhancements

- [ ] Social login (Google, Facebook, GitHub)
- [ ] Wishlist sharing
- [ ] Product comparison
- [ ] Advanced analytics
- [ ] Mobile app (React Native)
- [ ] AI-powered recommendations
- [ ] Live chat support
- [ ] Seller dashboard
- [ ] Subscription products
- [ ] Loyalty programs

---

**Last Updated**: 2026-07-13
**Version**: 1.0.0
