## `clojure:temurin-19-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:feeef533dfa4b229982197415e84aa23bd10a5119f7ae56a38f009202360d348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-19-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:78959c73880dd73b8aa5168ce42c88a17dfed4a1ab1864f7e6c5e614682218ba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.5 MB (303454316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:680d053e1e86bda0a4d3acae711984dee977f9ad48413784fe42d3049838ca17`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:43 GMT
ADD file:abc6873c98339a3c496cb75ec2528e65ebe1f20d2cea777033f86dcd55d73da5 in / 
# Tue, 15 Nov 2022 04:04:43 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 17:50:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 18:00:19 GMT
COPY dir:fef581854733ec7202f8c807463b9e1952aeb6c7a002719c7e54987e50ea4dcb in /opt/java/openjdk 
# Tue, 15 Nov 2022 18:00:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Nov 2022 22:27:42 GMT
ENV CLOJURE_VERSION=1.11.1.1200
# Fri, 18 Nov 2022 22:27:42 GMT
WORKDIR /tmp
# Fri, 18 Nov 2022 22:27:58 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "694381cb78d44f143bdcc38657507f012ebac4009bc57cec67abef1675447878 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 18 Nov 2022 22:27:59 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 18 Nov 2022 22:27:59 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 18 Nov 2022 22:27:59 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 18 Nov 2022 22:27:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a8ca11554fce00d9177da2d76307bdc06df7faeb84529755c648ac4886192ed1`  
		Last Modified: Tue, 15 Nov 2022 04:08:24 GMT  
		Size: 55.0 MB (55038615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255e73ee1e6eea684a2802365781fb7b0537b3dd818cb1ce939242a8029132be`  
		Last Modified: Tue, 15 Nov 2022 18:12:23 GMT  
		Size: 201.1 MB (201103445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f20c1a68f7d6cb421cb6d35dc2b1110ef9853cf395f0fdf7747d1142811756`  
		Last Modified: Fri, 18 Nov 2022 22:37:38 GMT  
		Size: 47.3 MB (47311240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d667c5a7176e9602de1476b6d075e47101456740f8b434b91548ea9105d2239`  
		Last Modified: Fri, 18 Nov 2022 22:37:32 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495e20fb118eae99ddfcde2a38678f5f5b9fcadf28bf8dfbcfede8247086adc5`  
		Last Modified: Fri, 18 Nov 2022 22:37:32 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-19-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0919851cb45bdb6ba25fc9ef202808eed098c91249c795b9d2d07352ee620a2a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300869440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d6f8cf72bf442f7a37405a15e69b80d6fb1f3b0a91b453f28e36799b601f91`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:12 GMT
ADD file:1f3a7177f64e1adda3e7a541c93dd4322c6ecb4f00f7b015665df2c0c08b59a5 in / 
# Tue, 15 Nov 2022 01:41:12 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 05:48:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 05:56:38 GMT
COPY dir:4138443eebfda1a2a245638d5bb568645bd34d79b66d39a3be31b5ac6b823d6d in /opt/java/openjdk 
# Tue, 15 Nov 2022 05:56:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Nov 2022 22:45:56 GMT
ENV CLOJURE_VERSION=1.11.1.1200
# Fri, 18 Nov 2022 22:45:56 GMT
WORKDIR /tmp
# Fri, 18 Nov 2022 22:46:09 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "694381cb78d44f143bdcc38657507f012ebac4009bc57cec67abef1675447878 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 18 Nov 2022 22:46:09 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 18 Nov 2022 22:46:09 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 18 Nov 2022 22:46:09 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 18 Nov 2022 22:46:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:077c13527d405646e2f6bb426e04716ae4f8dd2fdd8966dcb0194564a2b57896`  
		Last Modified: Tue, 15 Nov 2022 01:44:12 GMT  
		Size: 53.7 MB (53699862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5fdef0df9660bc53c8d91dc032dd6670451891d34a69da37129f03671d76128`  
		Last Modified: Tue, 15 Nov 2022 06:06:38 GMT  
		Size: 199.9 MB (199864458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2d8168829e9149f193022cc0dee4814f100b0ac6c47f4d09fc9717f1f245d50`  
		Last Modified: Fri, 18 Nov 2022 22:53:48 GMT  
		Size: 47.3 MB (47304103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94227ec1568ee66c502e95f7096db43c684f5db7084f97897cf6ba4ac30b9c4d`  
		Last Modified: Fri, 18 Nov 2022 22:53:44 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233ae986b221b7a95f59792c6f6238e73d49b97685772ae7a620bca99a343f14`  
		Last Modified: Fri, 18 Nov 2022 22:53:44 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
