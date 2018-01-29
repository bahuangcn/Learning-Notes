# Annotation of Data Binding Library

在 Android 的开发文档中，我们可以看到 [Data Binding Library](https://developer.android.com/reference/android/databinding/package-summary.html) 共为开发者提供了八个注解，他们分别是：

* [Bindable](#bindable)
* [BindingAdapter](#bindingadapter)
* [BindingConversion](#bindingconversion)
* [BindingMethod](#bindingmethod)
* [BindingMethods](#bindingmethods)
* [InverseBindingAdapter](#inversebindingadapter)
* [InverseBindingMethod](#inversebindingmethod)
* [InverseBindingMethods](#inversebindingmethods)

## Bindable

```java
@Target({ElementType.FIELD, ElementType.METHOD})
@Retention(RetentionPolicy.RUNTIME)
public @interface Bindable {
    String[] value() default {};
}
```



## BindingAdapter

```java
@Target({ElementType.METHOD})
public @interface BindingAdapter {
    String[] value();
    
    boolean requireAll() default true;
}
```



## BindingConversion

```java
@Target({ElementType.METHOD})
public @interface BindingConversion {
}
```



## BindingMethod

```java
@Target({ElementType.ANNOTATION_TYPE})
public @interface BindingMethod {
    Class type();

    String attribute();

    String method();
}
```

## BindingMethods

```java
@Target({ElementType.TYPE})
public @interface BindingMethods {
    BindingMethod[] value();
}
```

## InverseBindingAdapter

```java
@Target({ElementType.METHOD, ElementType.ANNOTATION_TYPE})
public @interface InverseBindingAdapter {
    String attribute();

    String event() default "";
}
```

## InverseBindingMethod

```java
@Target({ElementType.ANNOTATION_TYPE})
public @interface InverseBindingMethod {
    Class type();

    String attribute();

    String event() default "";

    String method() default "";
}
```

## InverseBindingMethods

```java
@Target({ElementType.TYPE})
public @interface InverseBindingMethods {
    InverseBindingMethod[] value();
}
```



