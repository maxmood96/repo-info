## `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye`

```console
$ docker pull clojure@sha256:e202dbc2d9da4e09efe8cfa30989bc577877dcaee5b2348a099bd37bb5820f89
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:3f9ee76cc155dada1feadff15d581e5bd1b80005b55d7668d18fba87fc293dfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.0 MB (178046965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f0b04c728d35dae02646d2d65840644aa463841f53802bf19dcb207a2d7b42`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b6f830cd306f01980373f1e0120f2d00018fbe51a9506b7262f5d9e4bbda74f9`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 53.8 MB (53756115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a07c2152f86dbc5c5fceb837e90a5cc4c856c1d0d8974e4ac0b5dfc5dbdcbfda`  
		Last Modified: Tue, 21 Oct 2025 02:19:27 GMT  
		Size: 54.7 MB (54731316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b8b62fdda3bbce2f8b34a35aba58054fffa27911a7d4e80236daa772be8692`  
		Last Modified: Tue, 21 Oct 2025 02:19:26 GMT  
		Size: 69.6 MB (69558891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502fc0fb65249279360c98647eba1c901f72cd4d4846c4795a80e9e2c95e3894`  
		Last Modified: Tue, 21 Oct 2025 02:19:19 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a61c886db79a9f21acfba0b6a3967fa210c4360994b1b30e983faf57a33dac7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7531514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c568a5aaf76425758315f3d4864ce6f7e30132d423776b0ae8a8d7ed0bd7d6c`

```dockerfile
```

-	Layers:
	-	`sha256:5b09eb6ac63bd7e770b198b2d77609352a9201b9bb61d56f25824c722b6278da`  
		Last Modified: Tue, 21 Oct 2025 09:46:22 GMT  
		Size: 7.5 MB (7517277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e56400ec82b6539b24e16a0f3a3a495f86090a41dcdef8e4cb3d594c9fd5aecb`  
		Last Modified: Tue, 21 Oct 2025 09:46:23 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:533864297985783639da282271870bf28a7d459279a1fb585b48aa6910255ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.8 MB (175782163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b787b25945416b8d030b5f4297af606ff38e43ce382b413b1c5051b2b0f129b1`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0a72c4e347b74aa6a0086cf3d1d928528ab02577a17bff4e22366a7df681f564`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 52.3 MB (52257444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea3b98d8b9c09e04f6716e3d1fcaf2c2b5ece5157ad1d431a022f69ccada1e9`  
		Last Modified: Tue, 21 Oct 2025 02:25:20 GMT  
		Size: 53.8 MB (53835637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab224df15cf7d4898872d3b5d923f081b4f740a80da35f1480dffcfa04d08de`  
		Last Modified: Tue, 21 Oct 2025 02:25:20 GMT  
		Size: 69.7 MB (69688436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea78b3c528e8d72495b95f879b3e127bf9c92d0c205a94123ac2a81f2b495b4`  
		Last Modified: Tue, 21 Oct 2025 02:25:15 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a68b0693bd9b15c06cb56f8123522f18fed6e4b5ce47acb7fd426bb4151dbc8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7537429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a845da09bcdb41ed4a7226ac5f251d965be9644a2c95ae5e5dfa26c651f3b6ba`

```dockerfile
```

-	Layers:
	-	`sha256:4e60c3cf9bc446d2a8bb7558cfec8f0ba83b290173032860a395e803f77fc1cd`  
		Last Modified: Tue, 21 Oct 2025 09:46:29 GMT  
		Size: 7.5 MB (7523074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9af4b600bdf79e0d7a495736d397220c402fdb9a94efa75e322363bb5f47a0b3`  
		Last Modified: Tue, 21 Oct 2025 09:46:30 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json
