## `clojure:tools-deps-1.12.3.1577`

```console
$ docker pull clojure@sha256:60bf1f03b6adaea5ed82de81772c5421b2a736758b5c25e707cc1b031e8b53f0
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

### `clojure:tools-deps-1.12.3.1577` - linux; amd64

```console
$ docker pull clojure@sha256:3598b7e7b71dc53d4daf51c8a3312a0a6001eb203a55c1a94904aff40c11c93c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221673461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a7d98b830e6b553e32f11666a5169e766f960bac03a1228d75db9226809b4c3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:56:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:56:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:56:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:56:27 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:56:27 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:56:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:56:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:56:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 23:56:42 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 23:56:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d4b068369f8e3902972f7e5cc1c6a6114a95168d566f0ac27ca4d35c6a4832`  
		Last Modified: Mon, 08 Dec 2025 23:57:24 GMT  
		Size: 92.0 MB (92045295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6994b44945cbac26e09697e875b9f99d7e91bcb33571d37a66c439dacd02b6c8`  
		Last Modified: Mon, 08 Dec 2025 23:57:20 GMT  
		Size: 81.1 MB (81146389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4f6abbc1d5b837062c042576d344da7b7c5d198c2ecb0c3c8b3de25a8777a9`  
		Last Modified: Mon, 08 Dec 2025 23:57:10 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5215783b918d57bfc4871e9e47f4f0114d3583745f56fac06263884142b929`  
		Last Modified: Mon, 08 Dec 2025 23:57:14 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577` - unknown; unknown

```console
$ docker pull clojure@sha256:53b79c3e722421eb50d7ab3c6d7f0dd303c40d861afd6292aa9c6f51f1074c98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7345325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f707d3695d9823232fa0f2c161e55692a299e6a60243052570c50667a2c28be6`

```dockerfile
```

-	Layers:
	-	`sha256:4c98105d2999186918947bbc1034dafcc40fb1e6309046d035bdf56e322626ba`  
		Last Modified: Tue, 09 Dec 2025 04:45:30 GMT  
		Size: 7.3 MB (7327554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61b6db2beeebba264b67ede67fd4fba7270e5e33ee24baffa01dbfd36e680201`  
		Last Modified: Tue, 09 Dec 2025 04:45:32 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.3.1577` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:17399e8ab9a6c412a327df67909b6c2ef603d359eb12dc93ed883bf01d92a2a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.4 MB (220443380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a51489114511284afc55a5d19823b4338de2a277f2a1c803e726bffb7aca7f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:03:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 00:03:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 00:03:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:03:41 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 00:03:41 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 00:03:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 00:03:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 00:03:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 00:03:56 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 00:03:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dff40d69ddf74c680cec3f177051d020e2f9b1c92c2567e38dcc79edda0bbc6`  
		Last Modified: Tue, 09 Dec 2025 00:04:41 GMT  
		Size: 91.1 MB (91052514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f42c74d750cf1cf9e9483d0632b80929ac9144e2f34ccfd8207612cb74e633d`  
		Last Modified: Tue, 09 Dec 2025 00:04:40 GMT  
		Size: 81.0 MB (81030757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a36895153194012fb29ad8343a6af9b9c84ff2e355bbd0e40356180d446768`  
		Last Modified: Tue, 09 Dec 2025 00:04:25 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6a8aace3a59628fe736a99832681abd7898789ef7380d922be0758b26f2e09`  
		Last Modified: Tue, 09 Dec 2025 00:04:26 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577` - unknown; unknown

```console
$ docker pull clojure@sha256:6c96a91227a43fb8422fdc810ab380678be796edc35f0f979bc568ae11558d40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7351347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dee277a595f52875748f734afded3d6315f47d9d0a3cbd0ad72f274aad23486`

```dockerfile
```

-	Layers:
	-	`sha256:d0cb2d66e3b452fb224f085e055cdfe91c876d40dc772fd83f2208d6c93d1b7b`  
		Last Modified: Tue, 09 Dec 2025 04:45:38 GMT  
		Size: 7.3 MB (7333386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c53fc0917678f2e42d68ec1227f5516c088f1693cd7d8cfdb8e3b7e3c7596bb`  
		Last Modified: Tue, 09 Dec 2025 04:45:39 GMT  
		Size: 18.0 KB (17961 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.3.1577` - linux; ppc64le

```console
$ docker pull clojure@sha256:ac932cc2e9c21ed1d859bfed13e641764bb2a83b65e8c4e566e6d18a73779f3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230924966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02a729bc6da2b1bc4f7eea8221b6bbda8f6eabdbbfef70033166601e6281747f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:34:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 22:34:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 22:34:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 22:34:22 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 22:34:23 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 22:47:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 22:47:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 22:47:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 22:47:41 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 22:47:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c088128ea77bb5c706bb00930020ea2fba147060275f49c5a7be6b54af5ca7c8`  
		Last Modified: Mon, 08 Dec 2025 22:17:06 GMT  
		Size: 52.3 MB (52326977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbeeb5c6058bd793bb98336cf15f96291626b642ff5b9461a0723bb0f77fc9eb`  
		Last Modified: Mon, 08 Dec 2025 22:36:56 GMT  
		Size: 91.6 MB (91610764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728cefd3d0455deac8bd62c99f0e77a95c7b758e833a9ee0118c176ee69aea93`  
		Last Modified: Mon, 08 Dec 2025 22:48:32 GMT  
		Size: 87.0 MB (86986184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76666e815cf634ad7c3e9aa75a42cf2268f6ecd29a3e758cad0beeda86d625f`  
		Last Modified: Mon, 08 Dec 2025 22:48:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb8d4d17d064d779c85ae98b85f977d61def5c378c617c0eb5fda82e93ad231b`  
		Last Modified: Mon, 08 Dec 2025 22:48:27 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577` - unknown; unknown

```console
$ docker pull clojure@sha256:bec0a3ac7cf44490408168c7a42ef3ef495358510f4a7a17a1c636b1d96cb670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7351957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0bd2ff6523b824d1187a73b1c3ccc6fcf04a34048cd83716cec3a134871cd4a`

```dockerfile
```

-	Layers:
	-	`sha256:3ec861f1923fd09e9a0d7dc8ad74cacf6a2dd95db1dd027904705c5fd204f0a4`  
		Last Modified: Tue, 09 Dec 2025 01:38:49 GMT  
		Size: 7.3 MB (7334102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:688292e8ea22b867d0e5a1316c09cd881f925abee9fa197eec321c6c79699fbf`  
		Last Modified: Tue, 09 Dec 2025 01:38:50 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.3.1577` - linux; s390x

```console
$ docker pull clojure@sha256:4df9cd39a62046766758d82bc2d6ccdc354b1a8c1a7ea77f69c2c641a5b65058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.3 MB (215306083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:791df794f7e3dc5e82650facc55d3f1a6f14f01e21a5b9390f3133e5218d0357`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 01:33:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 01:33:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 01:33:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:33:39 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 01:33:39 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 01:33:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 01:33:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 01:33:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 01:33:54 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 01:33:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f1896ba83f603ad81e0d8cb48b496e763b4b781a68efe11f1b6de9da929514ea`  
		Last Modified: Mon, 08 Dec 2025 22:15:09 GMT  
		Size: 47.1 MB (47137665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b901607e1053160f0c4a5999035c86877af07f0a5ab635c3250bef9051f1d4`  
		Last Modified: Tue, 09 Dec 2025 01:34:38 GMT  
		Size: 88.2 MB (88210741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede497669d640dd935258e6a9c4e17bc6224bdc87cb7bf36cdcdb421209ea590`  
		Last Modified: Tue, 09 Dec 2025 01:34:42 GMT  
		Size: 80.0 MB (79956641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ca221a862592fe47dc3d55089f9598a5172043cd281e42c31453bbdfe2784d`  
		Last Modified: Tue, 09 Dec 2025 01:34:35 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95ef072d3cbb3840af7a8a51e51e5c66313803ebe343b46670ff8ecbbcedb6e`  
		Last Modified: Tue, 09 Dec 2025 01:34:35 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577` - unknown; unknown

```console
$ docker pull clojure@sha256:de89f35989f2ce60c03e3873fd3eb44ea9c7b55398822b6b7b8b2542e666c136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7339192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb22e17c914d2df792247a9bf99824796b175381be774b459e637f842374c218`

```dockerfile
```

-	Layers:
	-	`sha256:c542d883fe979da77ac8fd154d3d2fb4f58867b9fff2b06485c9e893e00ff57c`  
		Last Modified: Tue, 09 Dec 2025 04:45:49 GMT  
		Size: 7.3 MB (7321421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c8d8ffd2da93c99c53fdda89daa56622a823740a685608fc58ae04ca2c291b6`  
		Last Modified: Tue, 09 Dec 2025 04:45:50 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json
