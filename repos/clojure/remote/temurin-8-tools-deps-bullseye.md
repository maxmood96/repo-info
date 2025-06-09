## `clojure:temurin-8-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:06cac7453b1945a68ee1d739b16d16f93763774766255b5333544d185ba3215f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:7e33d654b917617ec5450ed69a96c435472fdebae68c668d237570e8397cedbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177876773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbbd2a56ff8e58e2dcbbd984194bdc4ebcce25e5bf31176731c90a2db8fdc613`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a81836838c98b81f76df7b0fdfd187096b613e7574f6fd8d97cd5cb88029c5`  
		Last Modified: Mon, 09 Jun 2025 19:09:50 GMT  
		Size: 54.7 MB (54716180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4790823f16aaebecba672dbd49c1e7951f3bbdbcb548eb54154f42b1b8bafbb9`  
		Last Modified: Mon, 09 Jun 2025 19:09:52 GMT  
		Size: 69.4 MB (69409752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b237befb69f171576dfa4771bb01ad1659ba635b8ad1ee1a544da31a88be98d`  
		Last Modified: Mon, 09 Jun 2025 19:09:46 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7f257f125a019ee64ba9f14d2abe3f4cc701cb36387009e6688b2f6237f7040e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7533108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d08ec802034dd54f839227c22f916f9537c0c08c1e48c3a2de12fe30c019f4`

```dockerfile
```

-	Layers:
	-	`sha256:f6f5cf3fb26351a31fcc9cde2f312384362d9cb9cc2a87da4975b60deb721c63`  
		Last Modified: Mon, 09 Jun 2025 18:42:44 GMT  
		Size: 7.5 MB (7518872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0529c0e939737a57c8d37ac66660d12bddfec20e8ce979b4dd06e95c70d2049e`  
		Last Modified: Mon, 09 Jun 2025 18:42:45 GMT  
		Size: 14.2 KB (14236 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4556378b3a5e4f45def9261fbed36ce2d23b63cc18e09cc7da9965bd473522c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.6 MB (175616363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde8eb3f0410be535f2fe81e98bec5ea1f3f422fc0adb46c86230ea694fd7daf`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a5f701bfcb264810d9aa404e8040ce22b5b531c7f91508b60b5eea297f126c`  
		Last Modified: Tue, 03 Jun 2025 19:23:56 GMT  
		Size: 53.8 MB (53830516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090c55703a7acf2da976196d1d00d9f336c73c6c557c54596e96df6458c41ffa`  
		Last Modified: Mon, 09 Jun 2025 17:33:35 GMT  
		Size: 69.5 MB (69537447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ca4592240c3bfb0c86c06450829e97987d219df503221fe0af542023aa6f92`  
		Last Modified: Mon, 09 Jun 2025 17:33:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:01ac98b360d0c9b43d8ca854aa34e553a74459e1d11655ec89ba57de04b3f279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7539022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec740e690fd1c73fb6d27259d5db2656b0430e9630e8b37d298818d9a7944949`

```dockerfile
```

-	Layers:
	-	`sha256:5f65a78ad283564dd5dcf4b70cb0d3e5a14a17c1e1e3ff5996f9740608d6cb15`  
		Last Modified: Mon, 09 Jun 2025 18:42:51 GMT  
		Size: 7.5 MB (7524669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8818598b7df5a32f9cbb2b6fba687625e9aa0ddbd8fbf3a9787b41b862ee6f0d`  
		Last Modified: Mon, 09 Jun 2025 18:42:52 GMT  
		Size: 14.4 KB (14353 bytes)  
		MIME: application/vnd.in-toto+json
