## `clojure:temurin-17-tools-deps-1.11.1.1413-bullseye-slim`

```console
$ docker pull clojure@sha256:6e570437613b513376e31ac673e1d57a6ab75775f96e81d9d83794375e88cdb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-1.11.1.1413-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1d7d761de204e7319a7e606eb5a862efd5b3e59f38019dc007ed28af1a21f497
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.7 MB (237688841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10601dc293025d61a69f88d5ee82aba4ba2dc85910300d12b0070c49f4d671dc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:03 GMT
ADD file:7eb149bcaba1d7dcab06b3f9a0615ca459e9cb28459a0864f92b0037f270ba66 in / 
# Wed, 20 Sep 2023 04:56:03 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:22:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 Sep 2023 07:28:19 GMT
COPY dir:61bbef45bd137d5078f6a6f774d9bc49d275ae5fe27274294232d075ae1a5bf2 in /opt/java/openjdk 
# Wed, 20 Sep 2023 07:28:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 07:30:10 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Wed, 20 Sep 2023 07:30:11 GMT
WORKDIR /tmp
# Wed, 20 Sep 2023 07:30:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 20 Sep 2023 07:30:28 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 20 Sep 2023 07:30:28 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 20 Sep 2023 07:30:28 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 Sep 2023 07:30:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7dbc1adf280e1aa588c033eaa746aa6db327ee16be705740f81741f5e6945c86`  
		Last Modified: Wed, 20 Sep 2023 05:01:05 GMT  
		Size: 31.4 MB (31417711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f849626c60449d70414a79d12d1df3b48aa0c9fe4ae3176ba320531d57b9d3`  
		Last Modified: Wed, 20 Sep 2023 07:37:37 GMT  
		Size: 144.8 MB (144775758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cbc1fe3dacef4e44b38d32a6e0008d9dd709a88806db2d9ec35848b24227fbf`  
		Last Modified: Wed, 20 Sep 2023 07:38:41 GMT  
		Size: 61.5 MB (61494357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b7457373662ed3a8de29c822ac51ee7afc842cdb8ace3f82641f68a91a5ccb`  
		Last Modified: Wed, 20 Sep 2023 07:38:32 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9133f6c6c9c63362959ea4370d5c2313d2baac66f2a184a8ca95378fdd1fffa7`  
		Last Modified: Wed, 20 Sep 2023 07:38:32 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-1.11.1.1413-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:02589dcc09e40dfa5081f59c8771ee79018b10d917299d762f118ee36ae40f5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235218222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8cbebefa2d9aade9ede832517851dc7566fdfde953a3ccfb12e08bdb6d29607`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:53 GMT
ADD file:abd1ad48ae3ebec7a6ecc8ce3016c25be2afcbaedfcb904bc89b1ce59400aef0 in / 
# Thu, 07 Sep 2023 00:39:54 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 06:46:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 Sep 2023 06:46:35 GMT
COPY dir:ffc7dc4725a3524e0b294e59a90d1e58e69ec448374b50aef6bef0cfa219cb0f in /opt/java/openjdk 
# Thu, 07 Sep 2023 09:09:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 09:11:19 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Thu, 07 Sep 2023 09:11:19 GMT
WORKDIR /tmp
# Thu, 07 Sep 2023 09:11:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 07 Sep 2023 09:11:34 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 07 Sep 2023 09:11:34 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 07 Sep 2023 09:11:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 07 Sep 2023 09:11:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f96ab15157043879c2ff23e0556e798eba6a6ff3d7fd5d1384de223bb9f66f1d`  
		Last Modified: Thu, 07 Sep 2023 00:43:41 GMT  
		Size: 30.1 MB (30062903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0067a4775f017792de5f753490d0b5645640bc00f5c264295100a66ea689ec96`  
		Last Modified: Thu, 07 Sep 2023 06:48:31 GMT  
		Size: 143.5 MB (143543493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7861df1d9ffad3708c473360f34de5f947df9a42c9d4ff35466eaf9eb14710`  
		Last Modified: Thu, 07 Sep 2023 09:18:43 GMT  
		Size: 61.6 MB (61610807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84e6239775ee95e1eff4869864a4a78bd4a913e801017f5fa5aea3ea24b0e2c7`  
		Last Modified: Thu, 07 Sep 2023 09:18:37 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f4d8158495d5456b7f45a6f847504d1c2bd42d12ecd0650a6ebce8cbd8e161`  
		Last Modified: Thu, 07 Sep 2023 09:18:37 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
