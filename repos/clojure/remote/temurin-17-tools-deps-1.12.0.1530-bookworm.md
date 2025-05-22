## `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm`

```console
$ docker pull clojure@sha256:f0e0c0735284b5fa259666f1d75f14f18679b2bae36980f17ed6122bba0d4da3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:3eb4a55f38783b1e706f8cf25cdc20b2bb2d3f4339f6f41342357a80d1ed3ce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274119502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e3c94799da4d30efa7bb0d31f70596a080f044571a42105e0488038ee110f64`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Wed, 21 May 2025 22:27:42 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b5a3c25542e0d88809ba04c06354f605617015d471bc60c8bc0084925084a9`  
		Last Modified: Wed, 21 May 2025 23:33:06 GMT  
		Size: 144.6 MB (144634954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc6d0f46340222fb1f03d0033cd3e5b49275ea5e815876c126460e8c5a56620`  
		Last Modified: Wed, 21 May 2025 23:33:05 GMT  
		Size: 81.0 MB (80995262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe129bdb259639e11493b8217f0399cb0f10bc7038f5dc0c531eff363347dfd7`  
		Last Modified: Wed, 21 May 2025 23:33:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b9721aa43dad86c03b65eaee10b5e9f6318a2feda8b86e816fbb57bcbaefa44`  
		Last Modified: Wed, 21 May 2025 23:33:03 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b814b6613dbbc129d0bafccd392619edbb66d5c0199eed5e9777e050870c36a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7234343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0acd6454cd84750d5fbd54a2b65af822783b395cdea5679024c260da15913051`

```dockerfile
```

-	Layers:
	-	`sha256:24a00c32494f08bbad62c780ac9013859ec79df5af0ff22765ff49487f527d40`  
		Last Modified: Wed, 21 May 2025 23:33:04 GMT  
		Size: 7.2 MB (7218522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f26ec7d50bb902601975aca3b3505bfcb424366e7c8a1cee870d952e324576b2`  
		Last Modified: Wed, 21 May 2025 23:33:03 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:86065b823a92c34d2558af3bab7bfde57c68327cd32b7de472a69ac306445df8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.7 MB (272687487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2b931156ebb8a394410ae40218cb602db835a1957bc7716018645837886e3bb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010ef6cb6411a72cb9b7a87157534a1dd235611078bba6c262ef6f749557147e`  
		Last Modified: Thu, 22 May 2025 08:18:59 GMT  
		Size: 143.5 MB (143512648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab034bfe49534816a44f7956333671df05a572e02d89a83ab18c61d8c0752b0`  
		Last Modified: Thu, 22 May 2025 08:25:08 GMT  
		Size: 80.8 MB (80846620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3164fbc1f984b17e42e45d9eae92ea625cadcd0398caa308748a83756d5cec`  
		Last Modified: Thu, 22 May 2025 08:25:06 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea257e22b6c717319c046d6ec97e9aa4c1f8c1c0bcb412d640f988ef53985bc`  
		Last Modified: Thu, 22 May 2025 08:25:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:89f9d4b9bda1937373d7f5491894f0d1cdd49e5e82a885bd31c2f0919176e2ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7240224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a724c3254f3dbfb9a2658e1c77d2487cd3387f1f120213dd4b3a91eb2b7afc2f`

```dockerfile
```

-	Layers:
	-	`sha256:ef46ce5e8f97c872d818f6cbc611ecc54965a86b33b555aba37c6bc053398e6d`  
		Last Modified: Thu, 22 May 2025 08:25:06 GMT  
		Size: 7.2 MB (7224285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c573592f375492b03ee3be8b57d33bce57425a3b107069d228350fcb6edc31`  
		Last Modified: Thu, 22 May 2025 08:25:06 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:92da383f821b2d8161a17fec0b05b5c934238e9c698e420bd5d00d8967fb8571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.4 MB (283422795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6854b38dc9f5365fabf0b6a58dfb228b348eb2784638b3f76cc98f8709419b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Wed, 21 May 2025 22:27:49 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7b611fff1895e2aa9acd0368317ef57654ddad239e2abfe8e2c0ce77894c8f`  
		Last Modified: Thu, 22 May 2025 11:14:10 GMT  
		Size: 144.3 MB (144280512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce7db20df1ba10930974c9fbc4005c1274a2ef1e9dc6cc12fad6373819173a3`  
		Last Modified: Thu, 22 May 2025 11:21:29 GMT  
		Size: 86.8 MB (86809625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754abfb20349d010c4a4e6f4c4ce2db6f1e3dfa64ebb47133b28dac43fb586e0`  
		Last Modified: Thu, 22 May 2025 11:21:22 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff3f182cc5879920de76aabcce0e2d583b1844a24c8f78ea5e3850d9c9f41560`  
		Last Modified: Thu, 22 May 2025 11:21:22 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:fa332b6c9bfb6f684ee628ab73a05ff1352ca629a4f46a150db66761cdf2b286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7239595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e937203a33fcfc88d9607f33a555cf402c8604511bfbd224ec765d04604e80a`

```dockerfile
```

-	Layers:
	-	`sha256:e24e93f6f3fe891dac77b51bbb903d6f7e57eb6f2ca474ae5173ec3648377628`  
		Last Modified: Thu, 22 May 2025 11:21:22 GMT  
		Size: 7.2 MB (7223726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc199539cb51582835fb324b2df4bb15eabc1c1a47f4d7f27b6400017008437e`  
		Last Modified: Thu, 22 May 2025 11:21:21 GMT  
		Size: 15.9 KB (15869 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:a83366ff27db3150c169c0982b8bcb0ca4e9889fe406d452776bf17e57bf1265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261608743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d8dd420f55a66fda1e0cd6cb127e237b2de95c2cc3deec45e03afed0c3ed0d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Wed, 21 May 2025 22:28:14 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9c813a7e65d2034deaf8d72553c6f77f9d06392049a6e567e512b1efb6e191`  
		Last Modified: Thu, 22 May 2025 03:49:42 GMT  
		Size: 134.7 MB (134673562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b02bb9a89c9e3e9abc9c0fe1327dd52b37a7ddb8d4516484bf7851576e8768d`  
		Last Modified: Thu, 22 May 2025 03:53:35 GMT  
		Size: 79.8 MB (79790300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9766fe771a9d34f88be1dc6ca7c1bfca000fdb29adbc5e4c95f7fce647fb5f`  
		Last Modified: Thu, 22 May 2025 03:53:33 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9072c17388bba2c6f43263e0946a08a40ed5a367b51bd33d579d58de251a4cc7`  
		Last Modified: Thu, 22 May 2025 03:53:33 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d2ea50ec47c267969407a4157859bd51af217fb29e9a88fafd94a0c81b455319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7228554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1366308761a894b59d1ce5ab3cbb1e0be80e90de0b189328e93303ac656a0cf`

```dockerfile
```

-	Layers:
	-	`sha256:aba409aa8d5f0e2d1b06c69fc6a0850119b369ca65008fddbdf4c621731843da`  
		Last Modified: Thu, 22 May 2025 03:53:34 GMT  
		Size: 7.2 MB (7212733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:088e24e0f1ccc0196b91f06a6552b0c4f64e77c9c21bffa48c6a7de2962ec0a7`  
		Last Modified: Thu, 22 May 2025 03:53:33 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json
