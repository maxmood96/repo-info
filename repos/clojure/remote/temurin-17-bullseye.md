## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:15d88c9960ae31a3e9905635b2c599a78534b7a60189ad6567f6968f3b0d72d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:ea751a31abe5491e134203dbca8c941e38468fff56cb3c63e9d156f601dee696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (269011836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0cd8d5711de771a3c1e6f4537ac82a7a68f1dcf07c8acc0b9a6b011ba8c90ed`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:d2a2ac890c4f902560feaadaac9f36a9b844131c97453ecb90241cf525185196 in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:29f873e2e3f8f1b35ae4bee023807e71b6e16e714dbd1cbd19b3124c62e7634c`  
		Last Modified: Thu, 13 Jun 2024 01:25:49 GMT  
		Size: 55.1 MB (55099190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f8db631a072db5f4e41c5295d829d621d530dd25b41033a49ba0629ecf3752`  
		Last Modified: Thu, 13 Jun 2024 18:13:59 GMT  
		Size: 145.1 MB (145095063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4701c6bcc8346e277877e459425cb65b5fcee91f207fb1c26c00b74af5ac239`  
		Last Modified: Thu, 13 Jun 2024 18:13:59 GMT  
		Size: 68.8 MB (68816534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba223b51fe1f319ad2cbd5630603311ecf86fc990f10f8625adb3730eacd9b1`  
		Last Modified: Thu, 13 Jun 2024 18:13:57 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2832638c3797d1485d0f04c2559221cea1c1da16dfa6524b4434d607597780e`  
		Last Modified: Thu, 13 Jun 2024 18:13:57 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:23d2faf7e3d1bd8c908d11cda6acb4492779cbe574da1bb8597bc448c06dfaf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7015188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18a80c82f5e6e4f24a8bcf1a19246739e015729ab9e85ee43da8583a56d005e`

```dockerfile
```

-	Layers:
	-	`sha256:fc3953189fd9e3bf3d14620ff597b8f3883615acece60e47dd60fbd66191c2d0`  
		Last Modified: Thu, 13 Jun 2024 18:13:58 GMT  
		Size: 7.0 MB (6999751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1236446e408b8f9ffcb87de241d5a0548a9b813b9de93aaa3d641302a7a456b9`  
		Last Modified: Thu, 13 Jun 2024 18:13:57 GMT  
		Size: 15.4 KB (15437 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c93a37f3bd9b1e72bc45f47fd2f6f2888cb302d27ebdc08b6306333c0a2f5e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.6 MB (266562602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc817f9d97b2e6dc0705df00d873e8c3a5378073f57fd0fd3d8e65aaf603fd11`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:cd3edc79f93d09aa5daffba99cc698c3fe0e02348e8dc284ef466b7e6596e68c in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f975e52008de385eb513258b4912477b214cddf1c8e87877f85028d940bfcdae`  
		Last Modified: Thu, 13 Jun 2024 00:43:32 GMT  
		Size: 53.7 MB (53739581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35b9a117dce3baf466fa9787dba1af17514ff984a67a3707772c24adbb1266d`  
		Last Modified: Thu, 13 Jun 2024 11:37:05 GMT  
		Size: 143.9 MB (143892779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a32db85c6e0b2a3e85cc1b8de6994efc28465f5af4b3ed41cec6acb2c2073e`  
		Last Modified: Thu, 13 Jun 2024 11:40:16 GMT  
		Size: 68.9 MB (68929193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac05d23a8f89e2b02f581490a61d860ee738ecb588a60d6b69579968247b7094`  
		Last Modified: Thu, 13 Jun 2024 11:40:14 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250992366cbb749eaadaa3c7b87a211f654bd4b98c2b5280c63757bc93d80d63`  
		Last Modified: Thu, 13 Jun 2024 11:40:14 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:567b13d3e14c6e6ef5f4d5433455c9a4ee24b7a2f3ab45a27196112338a28069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7021448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1fdf5bde0d89488149a438e7eb622f1e08fe3cbc3f5146fbdbe6fead1f2e724`

```dockerfile
```

-	Layers:
	-	`sha256:d480a287626ae4ff053ffdd602f86d9d4b5a44c9ce81ffbbe3e5527f79d29d70`  
		Last Modified: Thu, 13 Jun 2024 11:40:14 GMT  
		Size: 7.0 MB (7005473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a83c4cd1d3549cf1d7b23a5ea68ecbabcfec5aea1d4fd70e17930a72c2c608c6`  
		Last Modified: Thu, 13 Jun 2024 11:40:14 GMT  
		Size: 16.0 KB (15975 bytes)  
		MIME: application/vnd.in-toto+json
