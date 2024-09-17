## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:8cf04f85dbecc9dbaecce6f2b0f0b31a2a5bdf126ab07689e5138686888acfab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bookworm` - linux; amd64

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

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

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

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3bb333b7d7bc50f1f5d2edf6094ce44c555fe9296d04ca69710e2a0991d91071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.3 MB (274336165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7443317cf6eda9a1401be6a74526de7320a2c1b0bd84d7dac8ccca7fd7b38da7`
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
	-	`sha256:ce7200d0857db89d07cbd5e5cb92b246c83e764f2907e18fd7164a637ac306e4`  
		Last Modified: Tue, 17 Sep 2024 04:30:16 GMT  
		Size: 144.0 MB (143959449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1827d445965700cf4dc8657fd4750f2e26f81b263c08e815c60cb0d19b3cce24`  
		Last Modified: Tue, 17 Sep 2024 04:36:41 GMT  
		Size: 80.8 MB (80790047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5170a9decf21bbc6754d9929b55ccf80c17390331ca139ce283522f1f46e5481`  
		Last Modified: Tue, 17 Sep 2024 04:36:37 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab4b5d43f90c1e376973fafb9521442c6f0c506d3893d520081df05c75735cd`  
		Last Modified: Tue, 17 Sep 2024 04:36:37 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2bb6bb7f905a6f2c390fff5cc00244e113b07a7d7bd4cf8b54781abfdddc6183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7029350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:104969e5f3f7381c1ce680146d51a3cc599d92c0b294f74cb33bc6ac7bfcb6eb`

```dockerfile
```

-	Layers:
	-	`sha256:cd205d6efe83241fd5da7d23bfd10745e1a71fdd9bc9acf4366d46496391ff82`  
		Last Modified: Tue, 17 Sep 2024 04:36:38 GMT  
		Size: 7.0 MB (7013374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cc0c9e36607c94f7f7cdfa349d15d7235e26b76354be020c6c70f2c80e63ca5`  
		Last Modified: Tue, 17 Sep 2024 04:36:37 GMT  
		Size: 16.0 KB (15976 bytes)  
		MIME: application/vnd.in-toto+json
