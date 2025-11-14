## `maven:3-sapmachine`

```console
$ docker pull maven@sha256:95fbcce22dbcfdbad957744645199d18998a8a501449208fbf496585c1d6c064
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `maven:3-sapmachine` - linux; amd64

```console
$ docker pull maven@sha256:7d2182c16d636fdb2430c2ef3f6600891109a9bd1141c46feeac974e40aad28d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.9 MB (284860197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab083a8b1d55a03fb0bb66214f6ae2576fb9e695cea589e95c7bf85f5374a7c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:37:25 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Thu, 13 Nov 2025 23:37:25 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 01:43:22 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:43:22 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 14 Nov 2025 01:43:22 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 01:43:22 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 01:43:22 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 14 Nov 2025 01:43:22 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Nov 2025 01:43:22 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Nov 2025 01:43:22 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 01:43:22 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Nov 2025 01:43:22 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Nov 2025 01:43:22 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 14 Nov 2025 01:43:22 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Nov 2025 01:43:22 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Nov 2025 01:43:22 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Nov 2025 01:43:22 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb65f3b3b66b3d1ba4a9cb176b3bbb9222dd94d1218a0bd018a1b95c406ce6aa`  
		Last Modified: Fri, 14 Nov 2025 01:42:33 GMT  
		Size: 220.4 MB (220429816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fea737250c7aaea6dc04c99650dc793ccec48956defff000309a2cd14036f6c`  
		Last Modified: Fri, 14 Nov 2025 01:43:45 GMT  
		Size: 25.5 MB (25462082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db23fd0f6d5d031c03ed4290fccca5f0031fc4fc367191d9a116ed0adb91acd`  
		Last Modified: Fri, 14 Nov 2025 01:43:42 GMT  
		Size: 9.2 MB (9242572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49fdcb9cbff82108cb88e772b7947165850a0e256b67d7adc2a0aff8f27544ac`  
		Last Modified: Fri, 14 Nov 2025 01:43:42 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbac36e97ad9420a240744475b2f2fd5eafc5f97705d1543bdc567ab35ecb55`  
		Last Modified: Fri, 14 Nov 2025 01:43:41 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:693033a3ccafa6790d2156e7f76f2db2cafffc05cd5e9837b374846f79d1d196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4328418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526a3339d05b0109d2735493f80655b3419c37069af6117480871a0b299ceec8`

```dockerfile
```

-	Layers:
	-	`sha256:e009057dc8dafc966e577576132e644a3f13ac2d1c4ccefe8cb0ce1279eeafe8`  
		Last Modified: Fri, 14 Nov 2025 03:32:25 GMT  
		Size: 4.3 MB (4310673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1444d070d12eaa8a37cf80371ce4b97db5ed22fe75a3b8fc68a5a48cc4ca1a24`  
		Last Modified: Fri, 14 Nov 2025 03:32:26 GMT  
		Size: 17.7 KB (17745 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:58f00e4ac05c5bcfb7bd566a0f4c5b41fd11ed13a721aee969c09ebaa3cf1402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.8 MB (281824336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b74ccae9445974731898fe4bd020d8e17ac150a0bb73d274abb67df40bf009`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:42 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Thu, 13 Nov 2025 23:36:42 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 02:00:12 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 02:00:12 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 14 Nov 2025 02:00:12 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 02:00:12 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 02:00:12 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 14 Nov 2025 02:00:12 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Nov 2025 02:00:12 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Nov 2025 02:00:13 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 02:00:13 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Nov 2025 02:00:13 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Nov 2025 02:00:13 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 14 Nov 2025 02:00:13 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Nov 2025 02:00:13 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Nov 2025 02:00:13 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Nov 2025 02:00:13 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6010e2e23970c6d32ac7f316bbae37bc4c141bff6adc9b6d7037a709f7cc4c`  
		Last Modified: Fri, 14 Nov 2025 02:00:00 GMT  
		Size: 218.2 MB (218186634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32dfffbe602dc2a445a69cb82cdee4bb121d2a52542a49d7b9cd09a5c224eaf8`  
		Last Modified: Fri, 14 Nov 2025 02:00:36 GMT  
		Size: 25.5 MB (25532132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de040122a9707bb251f61f6f4dcfb912f69e7050b49f8284898e08f7c90c29ba`  
		Last Modified: Fri, 14 Nov 2025 02:00:35 GMT  
		Size: 9.2 MB (9242572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859b237d216c00c1e1a833402e7becd04b5b043b9f84cdc5453ee8ba540109f3`  
		Last Modified: Fri, 14 Nov 2025 02:00:34 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64ca4b4301a9d451342470fc067baadd15313ccc779b79b05840165a21a7cc1`  
		Last Modified: Fri, 14 Nov 2025 02:00:34 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:f989458684c7a5efcceed0badf8c31fd039d4fa59190e86a0269869d99b2d175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4335165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abc0646c6cee40d59a490ee1c05b763f655e48e9da3a2475a269ddd518c8b48e`

```dockerfile
```

-	Layers:
	-	`sha256:efde979e8603f237d2701c684563b34a3cd6aa90eec483600163aa595dcede3c`  
		Last Modified: Fri, 14 Nov 2025 03:32:31 GMT  
		Size: 4.3 MB (4317240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc47fdf5174b0333e8f4389bc71320a3ed7c5dd7705eebabc3464ad8b06fbf93`  
		Last Modified: Fri, 14 Nov 2025 03:32:32 GMT  
		Size: 17.9 KB (17925 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine` - linux; ppc64le

```console
$ docker pull maven@sha256:19f7bc1d635aedf71060a2b51ae7c05ccfbcf49c44a503088e8dca92e32a3547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294792107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecab5e7d574f45ea07d16f199c9312ac358eafa2f91f4838657434aced7f7bdd`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:29 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:33 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Wed, 01 Oct 2025 13:02:33 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:17 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 21 Oct 2025 21:30:17 GMT
CMD ["jshell"]
# Sat, 08 Nov 2025 22:45:16 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 22:45:17 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 08 Nov 2025 22:45:17 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 22:45:17 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 22:45:17 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 08 Nov 2025 22:45:17 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 08 Nov 2025 22:45:17 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 08 Nov 2025 22:45:17 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 08 Nov 2025 22:45:18 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 08 Nov 2025 22:45:18 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 08 Nov 2025 22:45:18 GMT
ARG MAVEN_VERSION=3.9.11
# Sat, 08 Nov 2025 22:45:18 GMT
ARG USER_HOME_DIR=/root
# Sat, 08 Nov 2025 22:45:18 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 08 Nov 2025 22:45:18 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 08 Nov 2025 22:45:18 GMT
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
	-	`sha256:15f2d4c764de735d714d4d2ecf1a2b3580c5348fc3132b2447d62f95074c8d0e`  
		Last Modified: Sat, 08 Nov 2025 22:46:04 GMT  
		Size: 30.0 MB (29985825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421b9dd70d452dba64ac16f2649639a5d105d843d8e79795f3fb6fa41666cf0e`  
		Last Modified: Sat, 08 Nov 2025 22:46:02 GMT  
		Size: 9.2 MB (9242574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccdb5c2334b95ccb0df5473672f4a764b5765d80dc4718c0bcea4779ec2924c`  
		Last Modified: Sat, 08 Nov 2025 22:46:01 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b120285d3370919ea0de17b64c77aa0e81477b4033e53d514f3544fa87882c7`  
		Last Modified: Sat, 08 Nov 2025 22:46:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:9e84a21ef8afe3c93921955aba0468f35459dde7c5668800b69821650e1e1eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4326910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640647250e9af5fd5d55c6d8f1e743a5a8d64a3be715107e8821ae9896f1c0cc`

```dockerfile
```

-	Layers:
	-	`sha256:41c557f3c27f726f5653a665f0e36465e6e497b4aa55cb345ff8f1a5bddeb3b2`  
		Last Modified: Sun, 09 Nov 2025 00:29:22 GMT  
		Size: 4.3 MB (4309091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a8c397348fa57aa579d23975c3801824acab18e3f62bfa592a2b627391404de`  
		Last Modified: Sun, 09 Nov 2025 00:29:23 GMT  
		Size: 17.8 KB (17819 bytes)  
		MIME: application/vnd.in-toto+json
