## `clojure:temurin-8-tools-deps-1.11.3.1456-bullseye-slim`

```console
$ docker pull clojure@sha256:5f56b3fb3b17554b40bd3d14b1fd4616d7d076a3a32fc8b446206f9aa583e840
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.11.3.1456-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:75eb0d76714add4e0833d4a81f3ca485b7bd7323c77e0e172a8b8b4f7476652b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193647287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79f449137526aec1df3c06038b83a5b33e6f9e38de6b14de6d9259e5e2a4633`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
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
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b674dca13bd93a59653973a02c50ce2afbc975235d70f5c823f5bdd3843038c8`  
		Last Modified: Tue, 02 Jul 2024 03:02:47 GMT  
		Size: 103.6 MB (103600228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8934423ba0cca14da069de06406bbbce36798f5bdcf942c48e55b611ac79744`  
		Last Modified: Tue, 02 Jul 2024 03:02:47 GMT  
		Size: 58.6 MB (58624129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34fc436754e828362fdd0f8e39dcef96a72e6b394530c16f7fce53b559338706`  
		Last Modified: Tue, 02 Jul 2024 03:02:46 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.11.3.1456-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f871f30ddeb65e7783f81837d271ff3420e431cb91c3cca599847adb9f63737a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4945680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50106d77fa086673e7a028be26c108bb4bbd15880daf9dd879cfaec439c808d8`

```dockerfile
```

-	Layers:
	-	`sha256:0645b18fd1e44d09a462d4660aa860f328f6b558b1fdc3594acaff4966a52931`  
		Last Modified: Tue, 02 Jul 2024 03:02:46 GMT  
		Size: 4.9 MB (4931760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94752d157fe90d508786f8cb21d0a6eba03886bc5e55fb5046bcbdba95dd9a15`  
		Last Modified: Tue, 02 Jul 2024 03:02:46 GMT  
		Size: 13.9 KB (13920 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.11.3.1456-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4108a10f42381cd53718f4e8c531943983d120f0c6885c2d0175bf6993697fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191328065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:497c58908024095393e9fbd9a14e0cf020747d837dedd8109c09c57f5b9154b8`
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
	-	`sha256:63746f18f87c6c5edfb5273077b2d3e8efce93a8af63851a1486eeacee35e18f`  
		Last Modified: Thu, 13 Jun 2024 11:23:06 GMT  
		Size: 102.7 MB (102700390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e0ca6b96a5e5c31da1ec13f3cc00d7abc9a72a08bae40fd7afa4ee47c5d7c6`  
		Last Modified: Thu, 13 Jun 2024 11:27:25 GMT  
		Size: 58.5 MB (58540052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72db153c5a11c5270f9d96195bb261b4856c1e3b908b36311b2fa471ef682847`  
		Last Modified: Thu, 13 Jun 2024 11:27:24 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.11.3.1456-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ae7d0e54fb0ca563ee663635a3d28be3e058021ff17c051fab415bde9df074c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4952537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14836c68e7c7972e05569fbfb062e2073d747f524514e18b4075f6520e93896e`

```dockerfile
```

-	Layers:
	-	`sha256:28427619180bfa8f2e43f3acbdacfe5519f5d2551538615bb50c5fe587b57b1d`  
		Last Modified: Thu, 13 Jun 2024 11:27:24 GMT  
		Size: 4.9 MB (4938077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:760d3940cf5ce0779cfb2526563656e37be347a023787a3cc3cbec4e3eb7a11b`  
		Last Modified: Thu, 13 Jun 2024 11:27:23 GMT  
		Size: 14.5 KB (14460 bytes)  
		MIME: application/vnd.in-toto+json
