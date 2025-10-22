## `maven:3-sapmachine-25`

```console
$ docker pull maven@sha256:76c93df9336a221a6482da8220691a54c50b608913833582b1bdcf9a8c661cc9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `maven:3-sapmachine-25` - linux; amd64

```console
$ docker pull maven@sha256:27bc0021461ddd10522c23db05ee83bc35af798afd0815ad969c88e975ef8501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.9 MB (284858650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:847aac5c1205df46ea2556935afb4074d77b4f9d986299ac714b1ca220507162`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 19 Sep 2025 20:27:44 GMT
ARG RELEASE
# Fri, 19 Sep 2025 20:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 19 Sep 2025 20:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 19 Sep 2025 20:27:44 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 19 Sep 2025 20:27:44 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Fri, 19 Sep 2025 20:27:44 GMT
CMD ["/bin/bash"]
# Fri, 19 Sep 2025 20:27:44 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Fri, 19 Sep 2025 20:27:44 GMT
CMD ["jshell"]
# Fri, 19 Sep 2025 20:27:44 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 19 Sep 2025 20:27:44 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 20:27:44 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 20:27:44 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 19 Sep 2025 20:27:44 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 19 Sep 2025 20:27:44 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 19 Sep 2025 20:27:44 GMT
ARG USER_HOME_DIR=/root
# Fri, 19 Sep 2025 20:27:44 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 19 Sep 2025 20:27:44 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 19 Sep 2025 20:27:44 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcfc77348e4d1c8aadf49e5cb7aaf67a47e20832ddd2e2acc289a6d2daf0e50`  
		Last Modified: Wed, 22 Oct 2025 05:49:12 GMT  
		Size: 220.4 MB (220429816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc4d7b635c61ac96db623d94a3871db4b53882b5c92b5bdb253c0e1f857f65d`  
		Last Modified: Wed, 22 Oct 2025 05:50:19 GMT  
		Size: 25.5 MB (25462057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a5ac747e6ff6f9bc490ca0b35d855f761086b1214356a585230674892f0bdd8`  
		Last Modified: Wed, 22 Oct 2025 05:50:18 GMT  
		Size: 9.2 MB (9242595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe54699bb62897ade93c259c5789ee0c7f40cb67a78804e99f2334244b11549`  
		Last Modified: Wed, 22 Oct 2025 05:50:18 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6fb209bfb760f74b46f9d87116f14a34ac971486c059691c202fa01ac3566b`  
		Last Modified: Wed, 22 Oct 2025 05:50:18 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-25` - unknown; unknown

```console
$ docker pull maven@sha256:5b383da0bc54e61d0bab1f4bdd87e5185ec4ea0d623286cfe1e82dd1aea5e042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4328461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6ef07c5157f9fcd6866129dcdb50ad274ceba5a8536abb4448a2cd8d6103b66`

```dockerfile
```

-	Layers:
	-	`sha256:f1a225b3bc1548dd15e45107194731ac251043b572a4f6a2405f96dab92b8047`  
		Last Modified: Wed, 22 Oct 2025 08:27:49 GMT  
		Size: 4.3 MB (4310673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5dd04b98f5c4e712f81b9a80805f173b90ebde40d8de939125a5146ce62eb01`  
		Last Modified: Wed, 22 Oct 2025 08:27:50 GMT  
		Size: 17.8 KB (17788 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-25` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:87ca3a5a324b3e2b4899dfdf5bdb1d460086b5d366863fd685b5d8b29d3d5a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.8 MB (281824767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f61ee5583dce0f3b7e9e0e954e7fbb083d9256820c582442d3328ced7a8a81`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 19 Sep 2025 20:27:44 GMT
ARG RELEASE
# Fri, 19 Sep 2025 20:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 19 Sep 2025 20:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 19 Sep 2025 20:27:44 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 19 Sep 2025 20:27:44 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Fri, 19 Sep 2025 20:27:44 GMT
CMD ["/bin/bash"]
# Fri, 19 Sep 2025 20:27:44 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Fri, 19 Sep 2025 20:27:44 GMT
CMD ["jshell"]
# Fri, 19 Sep 2025 20:27:44 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 19 Sep 2025 20:27:44 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 20:27:44 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 20:27:44 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 19 Sep 2025 20:27:44 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 19 Sep 2025 20:27:44 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 19 Sep 2025 20:27:44 GMT
ARG USER_HOME_DIR=/root
# Fri, 19 Sep 2025 20:27:44 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 19 Sep 2025 20:27:44 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 19 Sep 2025 20:27:44 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157ce77536b5daf0347576278dd3fb0a406c2799910b78b4b87e76df67eb7ebb`  
		Last Modified: Wed, 22 Oct 2025 00:10:50 GMT  
		Size: 218.2 MB (218186919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8497c888884918893484bb32e2702386f1c3e1ef1629bd6797dfaee9a5da3d`  
		Last Modified: Wed, 22 Oct 2025 00:10:51 GMT  
		Size: 25.5 MB (25532509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf865e9810d141aa2d199da385c35208b9e3c8860c3b6a8fc0937e669f8c55d5`  
		Last Modified: Wed, 22 Oct 2025 00:10:48 GMT  
		Size: 9.2 MB (9242586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c052b2303260fa35de24815bd6f9f419d06935d3395b1c0e0575abd4f61e27`  
		Last Modified: Wed, 22 Oct 2025 00:10:48 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b47e1807ea2f1897201c9139c07d25bb0c67deb7067e2ff3e9265bc958a68e`  
		Last Modified: Wed, 22 Oct 2025 00:10:48 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-25` - unknown; unknown

```console
$ docker pull maven@sha256:32120fd0dba97f2c2b6c78a2ab5c600a39252b1136757d3aa93bf4ebbf4e26ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4335208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282dfa469ea5d960d832c833308ee5f42ccaf8615ab44e2cc17e8b2244c848f9`

```dockerfile
```

-	Layers:
	-	`sha256:67742aeb067dc211f0950c005aa4889b6e7949d11bef73490d4fc1fc4e9ed55b`  
		Last Modified: Wed, 22 Oct 2025 02:27:58 GMT  
		Size: 4.3 MB (4317240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04adf4561716f41aebc565f1d1f45c06e9f68cb8fbd901d5d0bdcb82cca12ddd`  
		Last Modified: Wed, 22 Oct 2025 02:27:59 GMT  
		Size: 18.0 KB (17968 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-25` - linux; ppc64le

```console
$ docker pull maven@sha256:2ba239c3f393b07542152cf7554b06b9f81c64e1867c4c4cc583c93c8ef90c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294791896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4579547456d71240ed59b28268d86a89ca89b1745dc6032d2f38c275ef27c74a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 19 Sep 2025 20:27:44 GMT
ARG RELEASE
# Fri, 19 Sep 2025 20:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 19 Sep 2025 20:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 19 Sep 2025 20:27:44 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 19 Sep 2025 20:27:44 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Fri, 19 Sep 2025 20:27:44 GMT
CMD ["/bin/bash"]
# Fri, 19 Sep 2025 20:27:44 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Fri, 19 Sep 2025 20:27:44 GMT
CMD ["jshell"]
# Fri, 19 Sep 2025 20:27:44 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 19 Sep 2025 20:27:44 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 20:27:44 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 20:27:44 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 19 Sep 2025 20:27:44 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 19 Sep 2025 20:27:44 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 19 Sep 2025 20:27:44 GMT
ARG USER_HOME_DIR=/root
# Fri, 19 Sep 2025 20:27:44 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 19 Sep 2025 20:27:44 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 19 Sep 2025 20:27:44 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2447fd34f2a917b60d1990444663859bc6b67973aeffd76dffd9e967df5f9f5`  
		Last Modified: Wed, 22 Oct 2025 11:31:16 GMT  
		Size: 221.3 MB (221259144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6065c94cb5fe38abc16329a8f31e756113bd68f9a2cc1b44ea968d1477d6f0c`  
		Last Modified: Wed, 22 Oct 2025 13:29:08 GMT  
		Size: 30.0 MB (29985605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4df66eb238e0c168b7c55c4675f141750084aa8595d0a239c0c47ca1ba138b`  
		Last Modified: Wed, 22 Oct 2025 13:29:18 GMT  
		Size: 9.2 MB (9242582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d8254095e06e30ea721019a663f8b0a7db8db751653af110050dc51ddf7cd1`  
		Last Modified: Wed, 22 Oct 2025 13:29:15 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a0739b82be4e754611d85c96dd767d74aeac6f2b00c879199471f1a7687e97`  
		Last Modified: Wed, 22 Oct 2025 13:29:15 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-25` - unknown; unknown

```console
$ docker pull maven@sha256:7bfc2b9e15c6ba9776a556ebf99a5be9c1ee0f034570bb7b25bb1e14f51963a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4326953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c01003fde0f5fdbed0ded1d8990bca5027ebba8c6e8717a5feb63b2253974a`

```dockerfile
```

-	Layers:
	-	`sha256:72ec2d2b56888e37e6bee662b9444a2c621914dd98ae8ffbb70cf6250e3edc5b`  
		Last Modified: Wed, 22 Oct 2025 14:28:04 GMT  
		Size: 4.3 MB (4309091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2787a589025f9da3525508e98312669d5e791b741f9bfe16e85aaf9281bf7a21`  
		Last Modified: Wed, 22 Oct 2025 14:28:05 GMT  
		Size: 17.9 KB (17862 bytes)  
		MIME: application/vnd.in-toto+json
