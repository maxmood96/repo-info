## `clojure:temurin-8-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:0ee2feb3a30f86702b31f5bc97bffa8da2ef39360af8c14c25dfa137cc319909
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:65bb34a70de77e659368928d8889fc498935ed09bb35cc243f7f13bb64bd91ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.3 MB (156290007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ea2b56bf4ae1a93b844c2d0935c817caa72749c0548c0dded217510b4862bfb`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f7f88c6d7f710176d487a3ac59c7790f981832a06bfc197dbe4a74d73b1407b7`  
		Last Modified: Tue, 01 Jul 2025 01:14:56 GMT  
		Size: 29.8 MB (29761106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20b8a40a25e17a30957fcf4ffedfb0163e2149629a4ba1c7a7d440217cceea9`  
		Last Modified: Tue, 01 Jul 2025 02:38:00 GMT  
		Size: 54.7 MB (54716159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:921806a90955eee7b487afb7bbd3e95e1106aed313b61f07417aa83f0a362726`  
		Last Modified: Tue, 01 Jul 2025 02:38:02 GMT  
		Size: 71.8 MB (71812098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660e0b734fd7a0e57b29a86efce327e9d3517401c1f3cd3d0c5550fec06b66f4`  
		Last Modified: Tue, 01 Jul 2025 02:37:54 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d16706413cb912e61d5bf9a879ff8d6bdbace07fef48398ba35a1d1e46850bf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5388683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78d6e85e55fcbfd20ae7ac151553aabf387c4eb9e9531db9bd432183bd2d0718`

```dockerfile
```

-	Layers:
	-	`sha256:72e0f856d7bad0b86f0734876247bbb08076196ffd39023bbfcc0788d5ea7f40`  
		Last Modified: Tue, 01 Jul 2025 06:43:21 GMT  
		Size: 5.4 MB (5374412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15d303ab38d9d75d89dade4ef6716679321db1c95f74e27ac041bf0bcbbb0281`  
		Last Modified: Tue, 01 Jul 2025 06:43:21 GMT  
		Size: 14.3 KB (14271 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:15de362520b8a7034680b1a15aae03fbfbde102d6e5e485ee98c625b8962105e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.6 MB (155619447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e4f6b7a56d424039ad2d313b37153a0ade479a8cec69c95f0c0476c24d380d`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c3306e90503bf56d5d575fca0323e4953fc66cffec788094159d11570a81151f`  
		Last Modified: Tue, 10 Jun 2025 22:53:04 GMT  
		Size: 30.1 MB (30121041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780454c5132e789d94ec2c5838835a3c8e9d85cc31e3bd6119b346d1bdbf30a9`  
		Last Modified: Wed, 11 Jun 2025 08:13:37 GMT  
		Size: 53.8 MB (53830509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afe907a89e5ab4af9268552cf247f1cfa64361b135acfacf9bda97f55582351`  
		Last Modified: Wed, 11 Jun 2025 12:06:56 GMT  
		Size: 71.7 MB (71667252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c31be3e5c0e318bf6dff2125d575a84eb341e8a276773d1c906990e691f957e`  
		Last Modified: Wed, 11 Jun 2025 08:13:47 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:053d3945744fc142f2ca1afa469c4ab7ebf0ccf2b417b7c4fe74b31e6fe8adf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5395264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:921ff3dfa9217a2c8c3a09d327248425c62bd6627908e142caaf54511a9e5515`

```dockerfile
```

-	Layers:
	-	`sha256:a9db54bcab4c6ffb074438b964762a50984f547c0212cb4701b0f85a52fc7109`  
		Last Modified: Wed, 11 Jun 2025 09:43:59 GMT  
		Size: 5.4 MB (5380875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e6c4fde549b43506ecdac0603d21c1f6be99eb2ce248afcb951a52b7c4af837`  
		Last Modified: Wed, 11 Jun 2025 09:44:00 GMT  
		Size: 14.4 KB (14389 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:ea98fd23d47444a2972d63931c940e034dbb2ed355c90a1e47df9d36a6cb5b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (162985778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e55393111d491f8b5d023b36f0235d2c224928ac442dda29019002fc81334875`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9851a8240d92395a99e35175026ad70b4eb50fb4e03132b209af1bf02a1fa307`  
		Last Modified: Wed, 11 Jun 2025 00:37:24 GMT  
		Size: 33.6 MB (33580925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe4dce34eb3ad2dc1baed8746361afda72fdb706d6456d2fdfe74e216c36089`  
		Last Modified: Wed, 11 Jun 2025 08:06:22 GMT  
		Size: 52.2 MB (52167968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab166037bf17bf579169d3cdb4307caf5f3c47fda1989918b096285991d72e2f`  
		Last Modified: Wed, 11 Jun 2025 08:11:41 GMT  
		Size: 77.2 MB (77236240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299696d8b2627e7783a61b698a7bd1b31aea9e8417cbb512f149d8c36f4998ec`  
		Last Modified: Fri, 13 Jun 2025 01:44:09 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:749c2a65e0bdc308f363a66e71381e425d5497665cb56ec09e91f9543dc858b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5393691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a5eb4841c42030cd36c50942028f55dff5d8a316f2d357b54cc6ff07e3bd4ba`

```dockerfile
```

-	Layers:
	-	`sha256:5cf4afcba42596d7ba23ce1a8e58d1df069b958d65b118d690312fb20a4ca995`  
		Last Modified: Wed, 11 Jun 2025 09:44:05 GMT  
		Size: 5.4 MB (5379372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17027f5440e814005edb6cb5ce024d02c17426c627f066850366e14845b6f2f7`  
		Last Modified: Wed, 11 Jun 2025 09:44:06 GMT  
		Size: 14.3 KB (14319 bytes)  
		MIME: application/vnd.in-toto+json
