EImageValidator
===============

Yii extension which Validates the uploaded image with types (jpg, gif, png...etc), min & max size (in kilo bytes, width and height. This extension can be used for different purposes depending upon your requirements.

**Requirements**

Tested with Yii 1.1.10 and 1.1.12. may work on other versions

**Installation**

* Extract the file under protected/components folder.

**Usage**

* Example usage with types:

```
public function rules()
{
    return array(
        'photo', 'EImageValidator', 'types' => "gif, jpg, png",
    );
}
```

* Example usage with types and error message:

```
public function rules()
{
    return array(
        'photo', 'EImageValidator', 'types' => "gif, jpg, png", 'typesError' => 'Types error message',
    );
}
```

* Example usage with min & max size (in kilo bytes):

```
public function rules()
{
    return array(
        'photo', 'EImageValidator', 'min_size' => 10, 'max_size' => 50,
    );
}
```

* Example usage with min & max size (in kilo bytes) and error message:

```
public function rules()
{
    return array(
        'photo', 'EImageValidator', 'min_size' => 10, 'max_size' => 50, 'sizeError' => 'Size error message',
    );
}
```

* Example usage with width and height:

```
public function rules()
{
    return array(
        'photo', 'EImageValidator', 'width' => 600, 'height' => 400,
    );
}
```

* Example usage with width, height and allowEmplty:

```
public function rules()
{
    return array(
        'photo', 'EImageValidator', 'width' => 600, 'height' => 400, 'allowEmpty' => 'true',
    );
}
```

* Example usage with width, height and error message:

```
public function rules()
{
    return array(
        'photo', 'EImageValidator', 'width' => 600, 'height' => 400, 'dimensionError' => 'Image dimension error',
    );
}
```
