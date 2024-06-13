## `clojure:temurin-8-bullseye-slim`

```console
$ docker pull clojure@sha256:3503c41288769177ec3ae65d5f6879a3476b01c76cab19fcdb9eac71cf2ad98b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3b2be7257a33e929775d1d061253a09a4335ba536e2f4d63832e4d6b6df7f6dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.5 MB (193454417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a55fd2e0a651225cba2d468ead1aece892bac9355e9476cb61f87eceaddabf1`
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
	-	`sha256:21e12b95760a35d4c76eb751b062abf0b3ccbf8b606b9738ddb8a69aac67628e`  
		Last Modified: Wed, 05 Jun 2024 06:10:07 GMT  
		Size: 103.6 MB (103600201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6309a6be53354ca4b8eb42a27e631016d7254cd6f3d632be508409e65ec2bd77`  
		Last Modified: Wed, 05 Jun 2024 06:10:07 GMT  
		Size: 58.4 MB (58419636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214b2aed85635ec0caeb291b113a0ef7d123faaa15ff57fd04e9f4566225b818`  
		Last Modified: Wed, 05 Jun 2024 06:10:06 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6c8c1c2053c3c755774a570002ee069c9fab439ed7b8e263c1f18db41fd5e850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4945591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5746e5dbcebfc0bb6b4edaccd054e53d2792cd9e40559aac67725ddd4dd8ec18`

```dockerfile
```

-	Layers:
	-	`sha256:765c51b7556e9c9c49855a9cf3faa1c92de9aa14df2ab4d2c0069e148d583791`  
		Last Modified: Wed, 05 Jun 2024 06:10:06 GMT  
		Size: 4.9 MB (4931721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec4c2d444c2326198af864d044dd619f1165ba2e65faf7e61b169d1143c4245b`  
		Last Modified: Wed, 05 Jun 2024 06:10:06 GMT  
		Size: 13.9 KB (13870 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye-slim` - linux; arm64 variant v8

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

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

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
