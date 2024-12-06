# django
from AUEB courses
from django.urls import path
from school.api.views import (TeacherListCreateAPIView, TeacherDetailAPIView, 
                              StudentListCreateAPIView, StudentDetailAPIView, 
                              CourseCreateAPIView, CourseDetailAPIView)
                              
                              #EbookListCreateAPIView

urlpatterns = [
    path('teachers/',          TeacherListCreateAPIView.as_view(), name="teacher-list"),
    path('teachers/<int:pk>/', TeacherDetailAPIView.as_view()    , name = "teacher-detail"),
    path('students/',          StudentListCreateAPIView.as_view(), name="student-list"),
    path('students/<int:pk>/', StudentDetailAPIView.as_view(), name = "student-detail"),
    path('teachers/<int:ebook_pk>/course/', CourseCreateAPIView.as_view(), name="teacher-course"),
    path('students/<int:ebook_pk>/course/', CourseCreateAPIView.as_view(), name="student-course"),
    path('courses/<int:pk>/', CourseDetailAPIView.as_view(), name="course-detail"),
    
]
