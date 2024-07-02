## `clojure:tools-deps-1.11.3.1456-bullseye-slim`

```console
$ docker pull clojure@sha256:3f082a25a3f5672a4395b4feb6f619b49383b53044db0127a76a379db57a78ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.11.3.1456-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a4b7d71664f1e0ae5bec3b6372f0776babae72a780d1c244e048bee9868e6dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.5 MB (248545275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb621942b952925ba1c5037373ad807ac9a9caad379e5afb02ed3230b25afca`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e65e7772ddc47fa298657e3ddfc0d13be08c5cbcffaf7a5c288a436c14992f`  
		Last Modified: Tue, 02 Jul 2024 07:07:16 GMT  
		Size: 158.5 MB (158497926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352ec17730bda8a56164ccafad2af78bcd80d3005dbdb5e71691449db147e6d6`  
		Last Modified: Tue, 02 Jul 2024 07:07:14 GMT  
		Size: 58.6 MB (58624023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8409092d418d646bd88f76667f6aa3f8c5a2d7e9e1e60eb3e4a6394b115982`  
		Last Modified: Tue, 02 Jul 2024 07:07:13 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2f2e2e41fc299fe4d990a463b5290051f7279d1692bcb7a427911480cd29d4`  
		Last Modified: Tue, 02 Jul 2024 07:07:13 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.11.3.1456-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bc0b7df9e3b933e41b9302114e298f1ffd3c20eaa7d9ba6056b379bd23b65562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4926183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be315c6ac2ade984f6fde0347e07001d76221cbcb1e7b3bc5c62ea667aeaa259`

```dockerfile
```

-	Layers:
	-	`sha256:e620cd9e767a83b71c9e7c9d0b7b2601b85e3512c15568361f082d5ef380cfb3`  
		Last Modified: Tue, 02 Jul 2024 07:07:13 GMT  
		Size: 4.9 MB (4909978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fed32f6c118690d0ed2bd7f3e83fb1b2b87053ef94ce69ef2e3d25ef01426d7d`  
		Last Modified: Tue, 02 Jul 2024 07:07:13 GMT  
		Size: 16.2 KB (16205 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.11.3.1456-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dee8ae5b601f07e15c6cc51e7e2c735a9effd92e27bb17ec3ef417cd57b37ac8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.5 MB (245480302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b43f151a26fcfa02c7d59c10f796fd00de506bbc27b7b44741eccdbe6f65658`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a71cde0a05bf2dbc2d58274a1b7596b81c24690f46a39f56dd0ad3aedea380`  
		Last Modified: Tue, 02 Jul 2024 09:38:16 GMT  
		Size: 156.7 MB (156665610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75edcc86bae9856a2a602af351e471cff5955ddcf7151fa67507462917f5b2bb`  
		Last Modified: Tue, 02 Jul 2024 09:41:54 GMT  
		Size: 58.7 MB (58744038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04597eb9b010d95b92e5b976975a26440cbe3a32b921982ad403126ad3076c99`  
		Last Modified: Tue, 02 Jul 2024 09:41:52 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77fca13951120f7988e68b31282e84d45f0883320411e858a2bb7f1a704d42d6`  
		Last Modified: Tue, 02 Jul 2024 09:41:52 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.11.3.1456-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5f29c6bfec867624c45fa159967a82d2a00fd12de47e039ffa908160ec7f5923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4933131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fccce7b15d4673701821354e9947a950c6de5febdaabfb8ef33e299ec26582cc`

```dockerfile
```

-	Layers:
	-	`sha256:e0ad627d3a57a2ec7f377e4b2d56990a42de53355b5424ca70ea86962aff94dc`  
		Last Modified: Tue, 02 Jul 2024 09:41:53 GMT  
		Size: 4.9 MB (4916358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f95ec608f9c4874cb5f349121bbddbe67340b2a8eeb9fe2869d2dcf58da23c89`  
		Last Modified: Tue, 02 Jul 2024 09:41:52 GMT  
		Size: 16.8 KB (16773 bytes)  
		MIME: application/vnd.in-toto+json
