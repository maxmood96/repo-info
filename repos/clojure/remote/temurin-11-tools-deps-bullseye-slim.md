## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:9b45a12dea0c5c15c2b4802dabfb40f945f25f3ecb062e433c3d4d648adba951
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:74d150dea63e919dddec907ce71b27aa676a8b47acb1c77e58cd7447312eafa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235359302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9032f2a1c65447ecc9098acd6f84633fff10faa0fde314d58b1962f6deabe5b2`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173559f4941d0f6fd9dad904f826952192d6d4459cfee940b5cd84cc874c8df9`  
		Last Modified: Wed, 05 Jun 2024 06:10:18 GMT  
		Size: 145.5 MB (145505194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0f5c2b298e7fbbb896132f5fbd737943b2670e1cec00a3451d48f07ce817ee`  
		Last Modified: Wed, 05 Jun 2024 06:10:17 GMT  
		Size: 58.4 MB (58419530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c791224dc5adc73ec2dab1c1fe36d90569edc92b9a602988da5025b471dfd5e`  
		Last Modified: Wed, 05 Jun 2024 06:10:16 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:df96679f3c39488398d4d335c2ee16b224ee9a64f6dbd93b10ea54f67270df5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4923119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c86e77e14a0f029f1da759969682d372e40b8fee298733f65a2d810458247a5`

```dockerfile
```

-	Layers:
	-	`sha256:bd715727d0a33b5716a6e456431580719e0228d4f31e1ea778fb755ea18e69f3`  
		Last Modified: Wed, 05 Jun 2024 06:10:16 GMT  
		Size: 4.9 MB (4909233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca47f96a0513350f78a757d6237f4333d7a578869be7dac8e82121cff7ed97cf`  
		Last Modified: Wed, 05 Jun 2024 06:10:16 GMT  
		Size: 13.9 KB (13886 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5cb4d4b804a96e1c047ae949477198150864832f4af765e38eafd4046c3c3d7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230931826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:253e10b4fdc49d6393579db542920493b2a1bc6bb2d28dd8a4b59e00f70b9c04`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5737b1460bc8700dc97acb941195e47f2f3d16b9162522c09d5187556fa3189a`  
		Last Modified: Thu, 13 Jun 2024 11:30:48 GMT  
		Size: 142.3 MB (142304050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0794c5acb4a7a4be257025cd6ae06fa3d1b01debe26cc3c73db14acd5331ae94`  
		Last Modified: Thu, 13 Jun 2024 11:34:23 GMT  
		Size: 58.5 MB (58540154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b788d12b968a713c02f38c0b49061ca606ac1a19b7bbc3d1061a1b863ea8ca3`  
		Last Modified: Thu, 13 Jun 2024 11:34:21 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:108531394cf948c1778717791f9c464dc975ce04449963e5b4107c9e1a627c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4930065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbe3e8f42f7fb941b08b81a32bf0076e5a2358ef8fa45a545edfe47ec1c50180`

```dockerfile
```

-	Layers:
	-	`sha256:4cbfb1d9a3a15333c6de643f86c5f74adc07742b4167dab72885c53428c4f403`  
		Last Modified: Thu, 13 Jun 2024 11:34:21 GMT  
		Size: 4.9 MB (4915589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da074b648789c61b10d6b271fee09dba3deb79d412fe12deaf224b64c4a82f4`  
		Last Modified: Thu, 13 Jun 2024 11:34:21 GMT  
		Size: 14.5 KB (14476 bytes)  
		MIME: application/vnd.in-toto+json
