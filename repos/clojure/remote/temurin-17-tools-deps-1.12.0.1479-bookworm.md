## `clojure:temurin-17-tools-deps-1.12.0.1479-bookworm`

```console
$ docker pull clojure@sha256:24dc8fb8b43f8d4d0afdb1196159236af04f788bfc04a54a52a0a9cd3f6f5ff3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1479-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:bc00270c8bc20c66b13aae14b7412f44888643e21db34fd68266fa1b285236e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.7 MB (275652736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f6ce332a6ac138c741fdd6945de285d74222c6180daf930bb7222ce27737cd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:36 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Wed, 04 Sep 2024 22:30:36 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687d528a8302f1d475db520850649209c39942d60478c15a72db85b701f1d8bb`  
		Last Modified: Tue, 17 Sep 2024 01:56:51 GMT  
		Size: 145.2 MB (145166555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6226220be8fa13df7313e885d89045bb93a7b1a39a9834dd0b0a12e3b86616d`  
		Last Modified: Tue, 17 Sep 2024 01:56:48 GMT  
		Size: 80.9 MB (80928432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f4e66caa6b54aa718fe50f0deff2acb4adcf4529c42c9f383dff039570d843`  
		Last Modified: Tue, 17 Sep 2024 01:56:47 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec757aca84fff62a336a3cf731d2c370512d59bbccbbe81abf830c6c970ae97d`  
		Last Modified: Tue, 17 Sep 2024 01:56:47 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1479-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0e0d92d9d398359f6a2f11de747256442acdd681db826151d1e6e22a2ac5005c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7022427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5187dc69e01b6dcad12f13030d308b9bb7f291239714812025dd3cdb90c2f9a6`

```dockerfile
```

-	Layers:
	-	`sha256:15cfbc343be1d0ccff48a27b6158d2479ed6fc397090846ffb18e7cb6ad92009`  
		Last Modified: Tue, 17 Sep 2024 01:56:47 GMT  
		Size: 7.0 MB (7006987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:314a02d2c3b2683e1b5fee74eff5fdbf1fab61b6c348584b1fc7bd1cdf9e82d1`  
		Last Modified: Tue, 17 Sep 2024 01:56:47 GMT  
		Size: 15.4 KB (15440 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1479-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d24cb91982c6d7ba9de5019cbb1d2aa7778b8f86d9bf6fe92d63b159e434c19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.0 MB (273993566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a67f83acda517b6e14d6f8225b4fa13844ac546bf0106eebf735c897e9d8c687`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:42 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
# Wed, 04 Sep 2024 21:39:43 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4739aeebae48263039d4595d4e6ce54767ccaea2417dbd8daedf234bb19c713b`  
		Last Modified: Fri, 06 Sep 2024 21:19:53 GMT  
		Size: 144.0 MB (143959441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272ddd5bf7e056f82bcdb6f0c8d312b914a1721dd8ba4be8bc920f7961cc48d0`  
		Last Modified: Fri, 06 Sep 2024 21:25:54 GMT  
		Size: 80.4 MB (80447462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356456cb67b13885a66d588f4cfc698c314ff8953a1b26656b1df276d0ea7a41`  
		Last Modified: Fri, 06 Sep 2024 21:25:52 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0470412c98c29deaf4a3c516e428aea8f0d74579191fd3292f35a5df7dd8c4ed`  
		Last Modified: Fri, 06 Sep 2024 21:25:52 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1479-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:59dfa3af4d2f51970992d8506ccf11747acf6fa1de3777dd00fd88e865b21c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7021833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2a2f6e2a4ce572ff966f68f4a44ebaddb9bfc4d920f30b6a2685e2cea2fd3af`

```dockerfile
```

-	Layers:
	-	`sha256:2965afa56231ddbc895f4dbe1c7ec4ef51318b986963cf32e02d86fcedd851c1`  
		Last Modified: Fri, 06 Sep 2024 21:25:53 GMT  
		Size: 7.0 MB (7005858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfebca1c13ba0ae4273bfcdcb4f491f4f54437c9c74bcf9ec012f10ea8f14a09`  
		Last Modified: Fri, 06 Sep 2024 21:25:52 GMT  
		Size: 16.0 KB (15975 bytes)  
		MIME: application/vnd.in-toto+json
