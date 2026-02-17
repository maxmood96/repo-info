## `clojure:temurin-8-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:30b4035cc011067a46384919f93088e49e928cd9c955eb60cc006ccfa3e8b0dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2d436941fdeb3a3a459c60ef1f7581d9381f693d3f98bbd55b89220a8d722a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144565552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:816110ed04d1d5ceca0dfad44dcacf49c0fa63f92ef448f70fba46777a525d49`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 17 Feb 2026 21:40:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:40:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:40:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:40:49 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:40:49 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:41:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:41:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:41:02 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6621200eccdfc832b4adc987297325021879f086bd764612a44c87dab0f53d1a`  
		Last Modified: Tue, 17 Feb 2026 21:41:18 GMT  
		Size: 55.2 MB (55170110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b726e9f79669f4ce6746eba80a3f36c2e104b3a2196a4ece2f3df8071ebd2f9c`  
		Last Modified: Tue, 17 Feb 2026 21:41:19 GMT  
		Size: 59.1 MB (59136512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d8705b0236714e92cd64d80fc48c2c1a591ad44a52d1a9630d8d541dc59770`  
		Last Modified: Tue, 17 Feb 2026 21:41:16 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7d4301540051467190f7f082592e8a4448a283e9059a1df12f24c6866a2bbdd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5445355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:239208ac1a5ef8f7a75bcf93795b00c549a8544fc4c47c0c3f5a18886208b752`

```dockerfile
```

-	Layers:
	-	`sha256:287be0a8802c3ac8fb5dbd8fe3611f51024d9eb22d19e4161175c8c654eab3a7`  
		Last Modified: Tue, 17 Feb 2026 21:41:16 GMT  
		Size: 5.4 MB (5431107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1119c615ce43dc0b02d0e5f6875807bfe0c958b0991d0aae49b333beee5561f1`  
		Last Modified: Tue, 17 Feb 2026 21:41:15 GMT  
		Size: 14.2 KB (14248 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b068874b834aefd985456c2b7df4ff8fefb2129a249583c9ade8af2bf9e12a8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142284803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:922101b9e378ec7d0708477ff00afd6a0bfc0a6e0cc7180cc79154f61240192d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 17 Feb 2026 21:40:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:40:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:40:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:40:48 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:40:48 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:41:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:41:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:41:03 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102b20c645de84c5b26d4c8e8d58a59969be4f1b59ac3fff9a44103274a3a363`  
		Last Modified: Tue, 17 Feb 2026 21:41:20 GMT  
		Size: 54.3 MB (54251630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f16022e2a35c6a0191fb11cf1fffb3d918e6ec1252682ce92bc0b8ef88306f`  
		Last Modified: Tue, 17 Feb 2026 21:41:20 GMT  
		Size: 59.3 MB (59288088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a71b284998634951b3c00725a13aa1a0bf0a09ea080570a75d96b8266af922`  
		Last Modified: Tue, 17 Feb 2026 21:41:18 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:56ad2b2cceb3f5debff8212fadd841442791241a41afcea90c4ad872c6fe96b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5451905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:627f6a597a21f52fe05b8a416106a3e15ffce7ce0bfd35a178a1822a715734cb`

```dockerfile
```

-	Layers:
	-	`sha256:10cd66182b18afb13dcac00e304231f6b811b5779c8940b76d2f259e478724b9`  
		Last Modified: Tue, 17 Feb 2026 21:41:18 GMT  
		Size: 5.4 MB (5437539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80294afd633c57b2a3aa5a32ef398001861ed5aec45eafa3b8fc4f5547bcb72c`  
		Last Modified: Tue, 17 Feb 2026 21:41:18 GMT  
		Size: 14.4 KB (14366 bytes)  
		MIME: application/vnd.in-toto+json
