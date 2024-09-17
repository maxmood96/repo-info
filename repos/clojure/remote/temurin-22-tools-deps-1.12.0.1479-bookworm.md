## `clojure:temurin-22-tools-deps-1.12.0.1479-bookworm`

```console
$ docker pull clojure@sha256:9a4611bfa692caae4d3f84eda75b5aed27c646712a3f46080d85e8a3bbe16ed7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-1.12.0.1479-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:c336f9535338874b5ab229cfa3986295fa5fcaa0667db9cfbfcbee24f6cd5869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.0 MB (286967788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55095dc262fd80fde7156380de91f81f7ff9bae21163e9720e7b4120ce1729b0`
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
	-	`sha256:a5ef0ce3155d8f66cea5b8de382d101314072ffd7fadbf64a17e62b9bf53a07f`  
		Last Modified: Tue, 17 Sep 2024 01:59:20 GMT  
		Size: 156.5 MB (156481619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecc48659d1444f3cd13a22a99bf6771154333ed736455a71f3f31c5f50367ee`  
		Last Modified: Tue, 17 Sep 2024 01:59:19 GMT  
		Size: 80.9 MB (80928426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745c65159196c134fffb2d408b12cc1377841a94a210b58136173d213415a217`  
		Last Modified: Tue, 17 Sep 2024 01:59:18 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5386efb98b6cc4d122739d99a3d45271f193b617b8e816911432cc39026a03c7`  
		Last Modified: Tue, 17 Sep 2024 01:59:18 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.12.0.1479-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:68a5e1eeb62b42e5b4607557de206f60d90f80fff05b53dbe30ad49cbb9847a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7023789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45cb7c9cfdf7b908955ea00c2af8d697806033c192d83ae1e099f37654aafa10`

```dockerfile
```

-	Layers:
	-	`sha256:e147a7a84045e8df8961754832d0a8b5dccc68ecbde70968eabbe081b8068556`  
		Last Modified: Tue, 17 Sep 2024 01:59:18 GMT  
		Size: 7.0 MB (7007665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:815cb6a8454bec12dfcf76bf6fd3e04c3df0257f50e7fdefc9c548997c3f86d6`  
		Last Modified: Tue, 17 Sep 2024 01:59:18 GMT  
		Size: 16.1 KB (16124 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-tools-deps-1.12.0.1479-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:78ade8bc18f9cc8871657bdfeef3ee480e358af2efa7271f34820194ea3fc5f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284537654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8062b11818892b04b30b3f86765a906b821eea78327affb75a15a1949475452`
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
	-	`sha256:0ef85e1ae411579c6244e8292bee16b65c142fc57f5e3b6a43444fc8fab9c9f3`  
		Last Modified: Fri, 06 Sep 2024 21:41:11 GMT  
		Size: 154.5 MB (154503717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478bc92b654d348eee56cb616ba1350044d108b86df24f6fde78c5900d6899c9`  
		Last Modified: Fri, 06 Sep 2024 21:46:45 GMT  
		Size: 80.4 MB (80447272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c466c3f9a87740a5d0bce71d6e7e6623108d751afc95715bdb8e27add014fd74`  
		Last Modified: Fri, 06 Sep 2024 21:46:43 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f785d70ce82ee93757863d12e3daf0a8b45dc4192f648193a22fe269f3bc1f`  
		Last Modified: Fri, 06 Sep 2024 21:46:43 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.12.0.1479-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:3958b9d624eaf061abeca6222cb75a86cbad69ed8606ebc844451d638a1c2dd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7023244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f4d102bc7b70df5e2e6de5c6ea9df5996e42a648f51762230191b75c83bb388`

```dockerfile
```

-	Layers:
	-	`sha256:c4a7a7a060452e79f86319df93917e5350956876eeaf945915619b1b0fcceb93`  
		Last Modified: Fri, 06 Sep 2024 21:46:43 GMT  
		Size: 7.0 MB (7006560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74e3bb8fe2a74a4a6da19106fc12288b0feedb253a74dc0af11d54f679838028`  
		Last Modified: Fri, 06 Sep 2024 21:46:43 GMT  
		Size: 16.7 KB (16684 bytes)  
		MIME: application/vnd.in-toto+json
