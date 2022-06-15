## `maven:3-sapmachine`

```console
$ docker pull maven@sha256:7ec01a772fb36e9e0d8a4957c5897dcdee0e8153079f62eb99bb13ead02f5ad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `maven:3-sapmachine` - linux; amd64

```console
$ docker pull maven@sha256:320eb26ec015f6f950684c2a33aa66babe169d789b53a475273d176baa6f2389
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.1 MB (275051984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c59457aad66f5fcd20f587cfcc2a9f83b862e5b50d18fe30e1a9bebe5855fa`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 01:58:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 02:00:02 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.3.0.1     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 02:00:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 07 Jun 2022 02:00:03 GMT
CMD ["jshell"]
# Tue, 07 Jun 2022 05:02:27 GMT
RUN apt-get update     && apt-get install -y curl git     && rm -rf /var/lib/apt/lists/*
# Wed, 15 Jun 2022 18:23:18 GMT
ARG MAVEN_VERSION=3.8.6
# Wed, 15 Jun 2022 18:23:18 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Jun 2022 18:23:18 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Wed, 15 Jun 2022 18:23:19 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Wed, 15 Jun 2022 18:23:27 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 15 Jun 2022 18:23:27 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 15 Jun 2022 18:23:27 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 15 Jun 2022 18:23:27 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 15 Jun 2022 18:23:27 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 15 Jun 2022 18:23:27 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 15 Jun 2022 18:23:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe776cde7ad2a2b7a4d2c92bae129822b7fe24c87f0491eb7c7e449bf80c59a`  
		Last Modified: Tue, 07 Jun 2022 02:01:02 GMT  
		Size: 7.9 MB (7926360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df80882928ff58941ceb49d0ab69d77503c243f2135390a07aadea5ea7f3462`  
		Last Modified: Tue, 07 Jun 2022 02:01:51 GMT  
		Size: 197.8 MB (197779312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426f6c32bb0347d5fbb256f2ea98b381ccf451eb016dad2498b3ea600e373464`  
		Last Modified: Tue, 07 Jun 2022 05:08:16 GMT  
		Size: 32.0 MB (32032987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ce314227a5ea391cb63b24b9fd9054488c03941df461c55a39af452e5e956d`  
		Last Modified: Wed, 15 Jun 2022 18:31:58 GMT  
		Size: 8.7 MB (8739480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d02d522d01f79f1ca34ed396c63cdd7ad36383062e460d8b0bb2807596e05234`  
		Last Modified: Wed, 15 Jun 2022 18:31:58 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9f03561126514684da1a73251f491a7677b0426879750d11e71c024ff9772f4`  
		Last Modified: Wed, 15 Jun 2022 18:31:57 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
