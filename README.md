    git clone git@github.com:sness23/cello-sequential.git

    docker run --rm -i \
    -v ~/cello-sequential/input:/root/input \
    -v ~/cello-sequential/output:/root/output \
    -t cidarlab/cello-dnacompiler:latest \
    java -classpath /root/app.jar org.cellocad.v2.DNACompiler.runtime.Main \
    -inputNetlist /root/input/subleq.v \
    -userConstraintsFile /root/input/Eco1C1G1T1.UCF.json \
    -inputSensorFile /root/input/Eco1C1G1T1.input.json \
    -outputDeviceFile /root/input/Eco1C1G1T1.output.json \
    -pythonEnv python \
    -outputDir /root/output

