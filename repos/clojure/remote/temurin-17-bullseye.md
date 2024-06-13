## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:0a8170f09db388762cec80bdfc4203f8160574ec6eaa53ae9fa89cfab9652eb8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:89dc7140d8b2f143d27bdce0dc76c6b14a32060d3758d4ad6c0eac86217ea3e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (269011202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6709afc1d63ff8f7110011bd2d7d6419a9fcd4f53bf759eaa58ba20ece107428`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:28:14 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 14 May 2024 01:28:14 GMT
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
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d53c5e6c23a46d782bcc9fbfbc4a31966196c4e6f342a89ac67368772b96dc1`  
		Last Modified: Wed, 05 Jun 2024 06:10:15 GMT  
		Size: 145.1 MB (145095120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad2a10360645a914f4b942ca3b1b972f1a6b92bae61b2fccdae462921c1ddf7`  
		Last Modified: Wed, 05 Jun 2024 06:10:17 GMT  
		Size: 68.8 MB (68815638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05c3202f0fd634b26ba405ee429d35957605dcb2fa19f50d90a1214d1eca018`  
		Last Modified: Wed, 05 Jun 2024 06:10:16 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c03020235d321b4b9121af5563d85705f6c55812fb134a32f073641bebf45a`  
		Last Modified: Wed, 05 Jun 2024 06:10:16 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1736c53415aae8fa99d5f44c99dfc17e9e848c2e55d1868a7a3508891434af5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7015141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84d4d0cff6d1f44fe17f4245b29ca833307c260b4d1bfb2640fd73e909e77450`

```dockerfile
```

-	Layers:
	-	`sha256:88413c049ccf8b0f9aa64d976d7d6ea6d53e1ef601dbd70946272fc93772683f`  
		Last Modified: Wed, 05 Jun 2024 06:10:16 GMT  
		Size: 7.0 MB (6999751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:070ea56f98e435770e29fb5e7483deacb75d60222abe5cdac2f433b49925aee4`  
		Last Modified: Wed, 05 Jun 2024 06:10:16 GMT  
		Size: 15.4 KB (15390 bytes)  
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
