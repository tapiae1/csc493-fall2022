# Architectural Design

Utility Functions

    loading(message: str, duration: int):
        Displays a loading message with a simple animation for a specified duration.

    make_image_dir():
        Creates a directory named 'generated_images' if it doesn’t exist.

    ask_for_images():
        Prompts the user to input the number of images and their size, returning these values.

    get_prompt(prompt: str):
        Prompts the user for a 'yes' or 'no' input and returns a boolean value based on the response.

Image Generation Functions

    generate_image(num=1000, size=10):
        Generates a binary image (NumPy array) of specified size with randomly placed ones, ensuring no adjacent ones.

    generate_multiple_images(num_images, size_images):
        Generates multiple images by calling generate_image in a loop, returning a list of generated images.

    save_image(image, idx, image_dir):
        Saves a given image (NumPy array) as a PNG file in the specified directory.

CSV and Data Handling Functions

    write_csv(images, num_ones):
        Writes the images and their corresponding counts of ones to a CSV file.

    make_csv_and_images(images, num_ones):
        Creates a CSV file and saves the images to disk, then visualizes the CSV.

    calculate_ones(images: np.ndarray):
        Calculates the number of ones in each image.

    visualize_csv():
        Visualizes the contents of the CSV file if the user consents.

    visualize_prepared_data(x: pd.DataFrame, y: pd.DataFrame):
        Visualizes the prepared data (features and labels) if the user consents.

    prepare_data():
        Reads the CSV file into a DataFrame, separates features and labels, and returns them.

    split_data(x: pd.DataFrame, y: pd.DataFrame):
        Splits the data into training and testing sets.

Machine Learning Functions

    build_model(training_x, training_y):
        Creates and trains a linear regression model on the training data.

    make_training_prediction(model_instance, training_X_set):
        Makes predictions on the training set using the trained model.

    make_testing_prediction(model_instance, testing_X_set):
        Makes predictions on the testing set using the trained model.

    evaluate_performance(Y_set, set_prediction):
        Evaluates the model’s performance using R2 score and visualizes the results.

    visualize_performance(training_Y, training_prediction):
        Visualizes the model’s performance by plotting the actual versus predicted values.

Main Function

    main():
        Coordinates the execution of the entire workflow:
            Prompts the user for the number and size of images.
            Creates the directory for images.
            Generates the images.
            Calculates the number of ones in each image.
            Creates a CSV file and saves the images.
            Prepares the data from the CSV.
            Splits the data into training and testing sets.
            Builds and trains a linear regression model.
            Makes predictions on the testing set.
            Evaluates and visualizes the model’s performance.
