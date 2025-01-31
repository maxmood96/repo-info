## `clojure:temurin-11-tools-deps-1.12.0.1501-bookworm-slim`

```console
$ docker pull clojure@sha256:b1ea79cf21458c326aa8437296a27f938c1491815769a353a7498087f961aae4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1501-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b41a5d0f609c7f415fe43884ce90d20e5ca9c2c31457576f9d14a3bdab078113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243346134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db75adddfe204fbb48ddf93d2e96550d015f030f5f7d5044f80c0a462c5eba4d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3482bf2d22e250d287b208ab06dad951df3adc043e34da21e8f4c6a0c0b4dc`  
		Last Modified: Wed, 29 Jan 2025 20:27:39 GMT  
		Size: 145.6 MB (145601447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5821f213a34ecd869e376eef1743e4e2d086de7b2a0b25c375a311be385e5bdd`  
		Last Modified: Wed, 29 Jan 2025 20:27:38 GMT  
		Size: 69.5 MB (69531626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8585f0cead85b4b61a017d1e0adce17ef3236210b701f1b571eacd14851229`  
		Last Modified: Wed, 29 Jan 2025 20:27:37 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1501-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4912ec464790b9bb8598346f7e711cebfd243ed83864293f29308e0b8a2b2743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4947018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff81a90a0fb2ec4185a64b933fc5780b87f6ec1ee1ab544457c3b6e60c84a380`

```dockerfile
```

-	Layers:
	-	`sha256:b9cdc7d07a21be0205f8ddeb45a9c6816d17e3a7df34bf3a844f209b9599bf02`  
		Last Modified: Wed, 29 Jan 2025 20:27:37 GMT  
		Size: 4.9 MB (4932708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3ebf217e00924cc0a8720d91a475b2cdf3a2e6a604735e4364d24ed29024537`  
		Last Modified: Wed, 29 Jan 2025 20:27:37 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1501-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3cc0950ceac6ddc9325907a6ac1e1c3a21c452df43f9b6a40745bc191b4553b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.8 MB (239812999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c439f5d58cac653042cc0fe7cef0de94208e256a36c1f947d1b51e9aa771459c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229927e0bbafdbde903dd88575e843117d316d1d8bcf9499da887ac21b6b14bb`  
		Last Modified: Thu, 23 Jan 2025 02:35:44 GMT  
		Size: 142.4 MB (142389489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e39981187bd7e07797a98c0cf4546b7db0f39c442ad140f664caa40b8e8ae90`  
		Last Modified: Wed, 29 Jan 2025 20:44:23 GMT  
		Size: 69.4 MB (69381834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06fdccc6d5e3016dc5cf552f616c155aa118edadf4865f81980e00214d8ec2f`  
		Last Modified: Wed, 29 Jan 2025 20:44:21 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1501-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6c989122148b3b1fce4208a34e6d8b1b49e11ddb248a75914015bd08baba9ab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4953515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1914db2893332006e8105cb560f1f42d9c4ad16b83387b0c1f5b178fb51e173`

```dockerfile
```

-	Layers:
	-	`sha256:eb6f95d871716bc5adf59d68cad078dab2793b96b4ef248a3656921bac6fcf2c`  
		Last Modified: Wed, 29 Jan 2025 20:44:21 GMT  
		Size: 4.9 MB (4939087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbb9783f0dc4df1dd3d3383a6bd9fde141ddb703ed45e2f58886878d44cc7d8f`  
		Last Modified: Wed, 29 Jan 2025 20:44:21 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
