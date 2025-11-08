## `maven:sapmachine`

```console
$ docker pull maven@sha256:bf4c435f5a70bd3129e0462df19e616bca170cdafe552f41350ad8d4efec2e38
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `maven:sapmachine` - linux; amd64

```console
$ docker pull maven@sha256:fd98485ec6a64b6f081f62834f9e2b88fcd0fe6c7b38eda389d5cc6cf2eed73d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.9 MB (284858654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1263dac064ee79c363efb04eb0ea0dd2dece6748b5f9351ea8918c903262c3`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:17 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 21 Oct 2025 21:30:17 GMT
CMD ["jshell"]
# Sat, 08 Nov 2025 19:25:20 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 19:25:20 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 08 Nov 2025 19:25:20 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:25:20 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:25:20 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 08 Nov 2025 19:25:20 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 08 Nov 2025 19:25:20 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 08 Nov 2025 19:25:20 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 08 Nov 2025 19:25:20 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 08 Nov 2025 19:25:21 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 08 Nov 2025 19:25:21 GMT
ARG MAVEN_VERSION=3.9.11
# Sat, 08 Nov 2025 19:25:21 GMT
ARG USER_HOME_DIR=/root
# Sat, 08 Nov 2025 19:25:21 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 08 Nov 2025 19:25:21 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 08 Nov 2025 19:25:21 GMT
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
	-	`sha256:b80ee5dd4e2a8fd0e292c4495ee5ca6ce6eed077c02a12f6f649990575a1c0f5`  
		Last Modified: Sat, 08 Nov 2025 19:25:49 GMT  
		Size: 25.5 MB (25462064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfa64278430b81320fd648650e25485fee9288975f5f4d8eb5bb886058010ac`  
		Last Modified: Sat, 08 Nov 2025 19:25:43 GMT  
		Size: 9.2 MB (9242592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c015bd1fc8f63cf0ae16591d8c1c9fa7710b9d1b53b4d7f12fd21d292f67efc2`  
		Last Modified: Sat, 08 Nov 2025 19:25:41 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9bee04c4833921ce7a9e5486cdba465f1c6064ef4d81d160f79eb605c461e2`  
		Last Modified: Sat, 08 Nov 2025 19:25:41 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:f72bc0f328e449db3d162cb0ee3f15905eb432e97a5d0174b3385210a85ad91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4328418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3914d955735c7e477075be4f49b848e357174ccbf182a82de959d5185f394cd5`

```dockerfile
```

-	Layers:
	-	`sha256:d157f70fcfb4c307a9e1c6291979579e96219485e7e13ac2a8d500281a4c9b14`  
		Last Modified: Sat, 08 Nov 2025 21:33:14 GMT  
		Size: 4.3 MB (4310673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74b9012a3d8b2274838f79809a2bf03e4ed168c8b0014eb6c106adab74ef210e`  
		Last Modified: Sat, 08 Nov 2025 21:33:15 GMT  
		Size: 17.7 KB (17745 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:sapmachine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:392ca529bf61512fea6e6dadbd2a330eaff2a320153b052aefe8a7b7518375d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.8 MB (281824560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfd0c1f990016b1d1b0be022f462a3850952c4eaf243fdb727f152c9c166ee64`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:17 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 21 Oct 2025 21:30:17 GMT
CMD ["jshell"]
# Sat, 08 Nov 2025 19:25:12 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 19:25:12 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 08 Nov 2025 19:25:12 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:25:12 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:25:12 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 08 Nov 2025 19:25:12 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 08 Nov 2025 19:25:12 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 08 Nov 2025 19:25:12 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 08 Nov 2025 19:25:12 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 08 Nov 2025 19:25:12 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 08 Nov 2025 19:25:12 GMT
ARG MAVEN_VERSION=3.9.11
# Sat, 08 Nov 2025 19:25:12 GMT
ARG USER_HOME_DIR=/root
# Sat, 08 Nov 2025 19:25:12 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 08 Nov 2025 19:25:12 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 08 Nov 2025 19:25:12 GMT
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
	-	`sha256:724c253688a0a85e56e6f86276be4879fabb3eb89501676ac6c803fc7bab7e9c`  
		Last Modified: Sat, 08 Nov 2025 19:25:35 GMT  
		Size: 25.5 MB (25532318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908924564da3943ce555401bf91762660f9adfc248e2bc29b7bce951d53981db`  
		Last Modified: Sat, 08 Nov 2025 19:25:34 GMT  
		Size: 9.2 MB (9242571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a624de3f6ab9e79ad5c1a3d190dc0942e0c3b2e900a5c3b8f5e24a89f0b48b28`  
		Last Modified: Sat, 08 Nov 2025 19:25:32 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2e25b4d86fb84b5222e5090b1c49fa615503f8f53f3554705fe1fd772ea80d`  
		Last Modified: Sat, 08 Nov 2025 19:25:32 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:8386fda67fb93e3e6ff613368b14a5f2c9b08208bdd9567a6cbe2cb076189588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4335166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d5502f2a13d29b2c229f33c319349b2b1475dd83648c84af772878a5860f057`

```dockerfile
```

-	Layers:
	-	`sha256:1f7db52866f4ee30ab67e677e10b0bc0e1145b6ee3b2215279f6b35aa06d9886`  
		Last Modified: Sat, 08 Nov 2025 21:33:19 GMT  
		Size: 4.3 MB (4317240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f3811b3d28ea8fde382baaf89e1fad2ff2a99d8d18b131a0485dca74cabd6d3`  
		Last Modified: Sat, 08 Nov 2025 21:33:19 GMT  
		Size: 17.9 KB (17926 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:sapmachine` - linux; ppc64le

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
		Last Modified: Thu, 23 Oct 2025 15:09:09 GMT  
		Size: 221.3 MB (221259144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6065c94cb5fe38abc16329a8f31e756113bd68f9a2cc1b44ea968d1477d6f0c`  
		Last Modified: Thu, 23 Oct 2025 15:08:52 GMT  
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

### `maven:sapmachine` - unknown; unknown

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
