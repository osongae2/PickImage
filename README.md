# PickImage
[![](https://jitpack.io/v/jrvansuita/PickImage.svg)](https://jitpack.io/#jrvansuita/PickImage)

This class was created to use in Android projects.

# Porpouse
Shows a DialogFragment with Camera or Gallery options. The user can choose from where provider wants to pick an image.

# Screeshot
![test](screenshot/img.png? "Dialog")

# Usage

#### Step 1. Add the JitPack repository to your build file:

    allprojects {
		repositories {
			...
			maven { url "https://jitpack.io" }
		}
	}

#### Step 2. Add the dependency

    dependencies {
	        compile 'com.github.jrvansuita:PickImage:v1.0.0'
	}

# Samples
 You can take a look at the sample app [located on this project](/app/).


# Implamentation

### Step #1 - Show the dialog.
    PickImageDialog.on(MainActivity.this, new PickSetup());

### Step #2 - Your AppCompatActivity have to implement IPickResult.
    @Override
      public void onPickImageResult(Bitmap bitmap) {
          //TODO: use bitmap.
      }

### Step #3 - Customize you Dialog using PickSetup.
    PickSetup setup = new PickSetup();
    setup.setBackgroundColor(yourColor);
    setup.setTitle(yourTitle);
    setup.setDimAmount(yourFloat);
    setup.setTitleColor(yourColor);
    
