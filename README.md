# Prediction-based-on-2D-data

<p>Model: 3 dense layers</p>
    <p>Database: Google carsData.json</p>
    <p>Library: Tensorflow.js</p>
    <p>CPU: AMD 3900X</p>
    <p>GPU: Nvidia 1080ti</p>
    
#    <p>Step1:Get the data from google</p>
async function getData() {

    const carsDataResponse = await fetch('https://storage.googleapis.com/tfjs-tutorials/carsData.json');
    
    const carsData = await carsDataResponse.json();
    
    const cleaned = carsData.map(car => ({
    
        mpg: car.Miles_per_Gallon,
        
        horsepower: car.Horsepower,
        
    }))
    
        .filter(car => (car.mpg != null && car.horsepower != null));

    return cleaned;
    
}
#    <p>Step2:Create model with three dense layer</p>

#    <p>Step3: Prepare the data for training</p>

#    <p>Step4: define the method of training for built model</p>

#    <p>Step5: test the performance of trained model</p>

#    <p>Step6: run algorithm</p>



    Some codes come from TensorFlow.js and I improve the performance of prediction by adding a dense layer, increasing times of epochs and batch size
