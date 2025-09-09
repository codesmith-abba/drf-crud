# drf-crud

A lightweight package that provides reusable CRUD (Create, Read, Update, Delete) views, serializers, and utilities for Django REST Framework (DRF). 

Stop repeating the same boilerplate code in every project!

---

## 🚀 Features
- Auto-generated CRUD API endpoints with minimal configuration.
- Generic base serializers and views.
- Easy integration with existing DRF projects.
- Extensible for custom logic.

---

## 📦 Installation
```bash
pip install drf-crud
```

EXAMPLE USAGE
```bash
# views.py
from drf_crud.viewsets import BaseModelViewSet
from myapp.models import Product
from myapp.serializers import ProductSerializer

class ProductViewSet(BaseModelViewSet):
    queryset = Product.objects.all()
    serializer_class = ProductSerializer
```
```bash
# urls.py
from django.urls import path, include
from rest_framework.routers import DefaultRouter
from .views import ProductViewSet

router = DefaultRouter()
router.register(r'products', ProductViewSet)

urlpatterns = [
    path('', include(router.urls)),
]
```




