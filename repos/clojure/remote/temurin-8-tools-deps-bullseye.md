## `clojure:temurin-8-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:221d10301b2df7717f60f4b12143db86679f245b0bf5438183a43a85ae67c0dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:30e18b65eaf3652dbb2f1612ffd492c1fbb473f9e00c97845b47f8d7e7033050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 MB (228028964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df75785101c5aa8166b1e5007a358ade6924c73cf0b6bb2ef834069dca6c7ead`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:56 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
# Wed, 04 Sep 2024 22:30:57 GMT
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8576aa2f5f1365f63cc94e151f0f7e9dce7ad18907183f35e2fa9cedb1a36618`  
		Last Modified: Tue, 17 Sep 2024 01:56:43 GMT  
		Size: 103.6 MB (103611898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562ef36e4eebeb2c89c12149db3695516dd7bef3fd0ee58723567e05c6649db2`  
		Last Modified: Tue, 17 Sep 2024 01:56:41 GMT  
		Size: 69.3 MB (69335088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3646412ded7834f618a87010e1c890df5198480fe37c740618a7f17c6ae20f47`  
		Last Modified: Tue, 17 Sep 2024 01:56:39 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:f9837fa63c0fe1c9874bfcbc9cf8f211fab27c6dcc9d4204772556745f4cc925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7079687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c22ba3040c21bbb4f8ce6ed2d957356f911b02f71039f79e26912ddf967d175`

```dockerfile
```

-	Layers:
	-	`sha256:b1f515be2475329162e10281f2f913991d9b8f45373fa52e49388631a0827247`  
		Last Modified: Tue, 17 Sep 2024 01:56:39 GMT  
		Size: 7.1 MB (7065835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:043f75b748bcb6639293a94a81f4258860583752aa0173190416299d32d79fbb`  
		Last Modified: Tue, 17 Sep 2024 01:56:39 GMT  
		Size: 13.9 KB (13852 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1cb6bfd2e9d08286291169a489b1b02780c6e9776b171bbefa112e503a59f86b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.9 MB (225928118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edd23f6c0fd7f4e96860dd8ee3af1ac163c4834ba68b7ec92d9af3a09112b41`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:59 GMT
ADD file:aad8b86b3a958bc07504985acedcc819faa4f1ed12ca8b46d8d94c4d564cbdfa in / 
# Wed, 04 Sep 2024 21:40:00 GMT
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:d82c4492ee91810a42e0c53e955a661e9a092364bc474c9db559ea5b24b7047f`  
		Last Modified: Wed, 04 Sep 2024 21:42:52 GMT  
		Size: 53.7 MB (53731619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93db4c8afc8a0890bd9b0a199dd8e132178a1acc07b8c47cbbe930bb3d0c96a4`  
		Last Modified: Tue, 17 Sep 2024 04:09:53 GMT  
		Size: 102.7 MB (102729218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cc48033e70845f23056e0d4df9b6acd7cc7ef27efd95481e98a469627df56b`  
		Last Modified: Tue, 17 Sep 2024 04:15:00 GMT  
		Size: 69.5 MB (69466636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d946f956a425d52145666c8f682ad8848c66aae46635404ac4d26c7736afb1a`  
		Last Modified: Tue, 17 Sep 2024 04:14:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:dc047b145c3ac8c8b3710754128dac798615ddf0b612dbdc10ac9f230f310574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7085944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f26a9c6e4e25ade9366baaf1ed2398599f8b239ec4aad953c644a27da7825c21`

```dockerfile
```

-	Layers:
	-	`sha256:68a78133c140deab7790fa6072e69a7cc6890dc7be2a01fa654267569a4f606f`  
		Last Modified: Tue, 17 Sep 2024 04:14:58 GMT  
		Size: 7.1 MB (7071557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac680ffd48397976a165d1cbb68b138610b7bc1b87a153f9f08198e9feb7755f`  
		Last Modified: Tue, 17 Sep 2024 04:14:57 GMT  
		Size: 14.4 KB (14387 bytes)  
		MIME: application/vnd.in-toto+json
