## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:eb78c59aae666bf24b53758f2248d6c742d63d31cdf67b366161554ecfdb46c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:0fe6816555f19bd10a2f8179eea7c1905cf31860dff7a80863f3051df790a3ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269198627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b502e8d00e0f179f491c5bb5186161320387149a6c1587a7a98145b4a88162f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
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
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563dda88c920889610be5bec35723bd127657339d77b1242df26650c7da00a4e`  
		Last Modified: Tue, 02 Jul 2024 03:03:09 GMT  
		Size: 145.1 MB (145095076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35fb346dbbffbb8c33009cbf11e331bc6547f02bfd00813a41b48e9a1b909c7a`  
		Last Modified: Tue, 02 Jul 2024 03:03:05 GMT  
		Size: 69.0 MB (69021147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc3cbe02795fd376db266fa45e3731642274f2a3006f7d04e18fbc736649ded`  
		Last Modified: Tue, 02 Jul 2024 03:03:03 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fb034ecf6d56570fbf651ad373608cf5d37c32a57fb52b7b511ae8d3d28d3f`  
		Last Modified: Tue, 02 Jul 2024 03:03:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:83b3e8dd4cf8647a5aadf51d297119e40afb4313d59d892c8dcfb9a4071a1795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7015229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb770432f17f9842c5e30c2b03e5eb10f461a8f82dd067279896c054f2c84ff`

```dockerfile
```

-	Layers:
	-	`sha256:a1088879ec69630b296cafe3258cbd423e62159c17bb822318cc880979108ce3`  
		Last Modified: Tue, 02 Jul 2024 03:03:03 GMT  
		Size: 7.0 MB (6999790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f0380bf8de1a7c9be813bf734cb7119b3ecfdc05a7338a613d2acc5f541fad0`  
		Last Modified: Tue, 02 Jul 2024 03:03:03 GMT  
		Size: 15.4 KB (15439 bytes)  
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
