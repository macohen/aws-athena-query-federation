FROM public.ecr.aws/lambda/java:11

# Copy function code and runtime dependencies from Maven layout
COPY target/athena-vertica-2022.47.1.jar ${LAMBDA_TASK_ROOT}
# Unpack the jar
RUN jar xf athena-vertica-2022.47.1.jar

# Set the CMD to your handler (could also be done as a parameter override outside of the Dockerfile)
CMD [ "com.amazonaws.athena.connectors.vertica.VerticaCompositeHandler" ]