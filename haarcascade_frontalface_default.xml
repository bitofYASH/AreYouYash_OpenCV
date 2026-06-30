import cv2

# Load Haar cascade for face detection
face_cascade = cv2.CascadeClassifier(cv2.data.haarcascades + 'haarcascade_frontalface_default.xml')

# Check if the cascade loaded successfully
if face_cascade.empty():
    print("Error loading Haar cascade.")
    exit()

# Open webcam (0 = default camera)
webcam = cv2.VideoCapture(0)

# Check if the webcam is opened successfully
if not webcam.isOpened():
    print("Cannot access webcam.")
    exit()

while True:
    # Capture frame-by-frame
    ret, img = webcam.read()
    if not ret:
        print("Failed to capture frame.")
        break

    # Convert to grayscale
    gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)

    # Detect faces
    faces = face_cascade.detectMultiScale(gray, scaleFactor=1.1, minNeighbors=5)

    for (x, y, w, h) in faces:
        # Draw rectangle around the face
        cv2.rectangle(img, (x, y), (x + w, y + h), (0, 255, 0), 3)

        # Text to display
        text = "FACE DETECTED"
        font = cv2.FONT_HERSHEY_SIMPLEX
        font_scale = 0.6
        thickness = 2
        color = (0, 255, 0)

        # Get text size to center it
        text_size, _ = cv2.getTextSize(text, font, font_scale, thickness)
        text_x = x + (w - text_size[0]) // 2
        text_y = y + h + text_size[1] + 10  # Slightly below the rectangle

        # Draw text
        cv2.putText(img, text, (text_x, text_y), font, font_scale, color, thickness)

    # Show the resulting frame
    cv2.imshow("Face Detection", img)

    # Break loop on ESC key
    if cv2.waitKey(10) == 27:
        break

# Release resources
webcam.release()
cv2.destroyAllWindows()
