## `clojure:temurin-24-bullseye-slim`

```console
$ docker pull clojure@sha256:2c56c89146da631251d40a47c57f8ac5a115ec33b3e470134cd4701c2a5b9f2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:bbf2b9768a8b984f759dd98fd8c0eb6926bf43159d17524335028510bc649c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.4 MB (179383137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7916f02cac299353a217060c0e3add16941b1138fddd77841edf62778f442d7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:456a3213e1b1f193dc759cd05f6f8422428b8c4bd45ef40fbf41ba43bdce8570`  
		Last Modified: Mon, 08 Sep 2025 21:12:48 GMT  
		Size: 30.3 MB (30256068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9b2ed26602efa62f6c3175a7595c79af5c3aff78315124ad625fbe94531ac6`  
		Last Modified: Mon, 08 Sep 2025 21:44:04 GMT  
		Size: 90.0 MB (89975189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2612e12297af4ed4a0a7c729c14f4a2c3e3a23eb4b62a1109b67ca5e95f094d4`  
		Last Modified: Mon, 08 Sep 2025 21:44:04 GMT  
		Size: 59.2 MB (59150837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1f5a5d3c65ffb712915f56ae33527a2d9f0cc5055d542a0d37da4a3713c8a7`  
		Last Modified: Mon, 08 Sep 2025 22:59:12 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7851ca754190fe849d523023e0cc6b602f95ddd7372c2483ded33d90785f55`  
		Last Modified: Mon, 08 Sep 2025 22:59:11 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0eb0fafba6bcf858a2beb9086e56abcf9292556fbb2dcab10344830d12a13968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5274587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07a06d6a0084abef43887867cfd53c61ec0ac3caa92b0acbfbe502a0cf4dcf8e`

```dockerfile
```

-	Layers:
	-	`sha256:407963a38d363156656b6af4d6425afeadb57cf1deb2688f02552dace9a5bb74`  
		Last Modified: Tue, 09 Sep 2025 00:43:37 GMT  
		Size: 5.3 MB (5258715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d013e2d853cf8b3258b203f1f334fb41dcf022f59a29210c996e7191cc57d490`  
		Last Modified: Tue, 09 Sep 2025 00:43:38 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:208d486b4af54f8a1843a467f4cbd710f75277c61cf8259ed57e97977427e84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.1 MB (177126760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:063c26b16e9fdde0950fbfd2e5b9054c107df0efc23e7bcfd3824a906700b2ac`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b99ef417bc3eb3946e7b3162f6c19dbca1039f3b4124deb116c3a0ab763e65ad`  
		Last Modified: Tue, 12 Aug 2025 22:33:30 GMT  
		Size: 28.8 MB (28750491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23400f2f1e25d2d463cd21867bd53838dc5043e5e5e0b138a1b7d01be6f5fb52`  
		Last Modified: Wed, 03 Sep 2025 07:06:41 GMT  
		Size: 89.1 MB (89092530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff32ef14a50960571f42a9a7f200df3406af4ced9c6cb2bdefd8e3ebc6065cb`  
		Last Modified: Tue, 02 Sep 2025 08:30:07 GMT  
		Size: 59.3 MB (59282695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b3fc4104f99839d62155b96c394733ef57fa2fc552f3ea436b1894e2cd22b2`  
		Last Modified: Tue, 02 Sep 2025 08:30:01 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926d02c91baa3bab6761e0ba8b6b830594832687f30869736e7b1fa706b938e7`  
		Last Modified: Tue, 02 Sep 2025 08:30:01 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bf3bd48ce6269dff99202d85bc21683114db08c691cdbad89bf6a18bb627ebf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5280434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b422155444769e3416951af92f3ad96add912f585f44169978fa28ffc269ab0`

```dockerfile
```

-	Layers:
	-	`sha256:380201de195bbe23d2c35989785bba5ac027a0f1abfe8cb1e995e0f0452b02b5`  
		Last Modified: Tue, 02 Sep 2025 09:42:39 GMT  
		Size: 5.3 MB (5264444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:712da2f6d8b4cfc3154a239fefc318a813753ff71c8cf33fb9580e5cd14c633e`  
		Last Modified: Tue, 02 Sep 2025 09:42:40 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json
