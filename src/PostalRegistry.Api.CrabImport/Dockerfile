FROM mcr.microsoft.com/dotnet/runtime-deps:5.0.2

LABEL maintainer "agentschap Informatie Vlaanderen <informatie.vlaanderen@vlaanderen.be>"

COPY / /app
WORKDIR /app

RUN apt-get update && \
    apt-get install curl jq -y && \
    chmod +x ./init.sh

EXPOSE 3000/tcp
ENV ASPNETCORE_URLS http://*:3000

ENTRYPOINT ["./init.sh"]
