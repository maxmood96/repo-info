## `clojure:temurin-17-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:86219bbe183f4c8ffe29b12e6ff55466901034a70b855116713ed8de3f7df4f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:8439f157fcfe1f9872eae6b943c70e0cad4bf3a9dae5df32bf055cc894a5afbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269198514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dca4eaf3abb9069f9720c72c48d3e204adc5cdab8fd51fe831074757cf302e90`
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
	-	`sha256:6a0fcc1b964d92bdd956f2fbdb1db6a68ab39dbee1778e76d8b7c27bc94672c1`  
		Last Modified: Tue, 02 Jul 2024 07:07:17 GMT  
		Size: 145.1 MB (145095124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54554b76c64ce22cc5dc42bbf90e009e861892b3e32e0cb2d9dcca22cc16397b`  
		Last Modified: Tue, 02 Jul 2024 07:07:15 GMT  
		Size: 69.0 MB (69020987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9deb704a122a73e1851dac13b29b8085f790f697a71f61850ffed52daf2ed5`  
		Last Modified: Tue, 02 Jul 2024 07:07:13 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e671f2b6cd4eee5cbaa66a0248588bc4315316a02768c711be2a8f2b64e683`  
		Last Modified: Tue, 02 Jul 2024 07:07:13 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:89b6bf97a81ad895ba0a02a7bc5a8379afab3c7f5a97149a757476b6e82ef97e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7015229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eebdd2fc8c15077220da052c50849ff9827abbd836a69e2f74f011b9a9c99d5`

```dockerfile
```

-	Layers:
	-	`sha256:f0e45bbec48de181bbc18f18cc6fbb2dc5d856aace55918fde2739fb14bf8a1d`  
		Last Modified: Tue, 02 Jul 2024 07:07:13 GMT  
		Size: 7.0 MB (6999790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66895f955a22fe7700b304b95c16e74dcdb84af4c99c698acfca246630c023ab`  
		Last Modified: Tue, 02 Jul 2024 07:07:13 GMT  
		Size: 15.4 KB (15439 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b3cd9bf4993c3bb7b8f589cf6d0f9389e1a0670cda2a027383a8e0c7c288a14c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.7 MB (266749269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df5547bd1d1c892130007bba1e46ecf1a12d3937b695679d46e36cccf0da86b9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:4e98397394fc6db8fa55fb21c15dab09007b6ba883cb193f3a53f94480fee872 in / 
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
	-	`sha256:a4cd3ad66f7873241881d2ddd4efa6521034245e95e2b0b4a059817345151048`  
		Last Modified: Tue, 02 Jul 2024 00:42:43 GMT  
		Size: 53.7 MB (53721653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accd4022fd10bdf90d9867428728c11f63914bb907fb3d33669e944f902b3c49`  
		Last Modified: Tue, 02 Jul 2024 09:29:36 GMT  
		Size: 143.9 MB (143892757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12016a3d6377ce756a293000d43146da9853346d22b3c8dfb5dfd300e55c77b9`  
		Last Modified: Tue, 02 Jul 2024 09:33:56 GMT  
		Size: 69.1 MB (69133819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baec2ce90d4b77e36e1d96b640452090dfde07305f0d881a73e966bcc5e1919a`  
		Last Modified: Tue, 02 Jul 2024 09:33:54 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e83f46dd527d6d2e7bb5e5247728074e2fd1be571f2f1f4adb6bf2e2ec88ad`  
		Last Modified: Tue, 02 Jul 2024 09:33:54 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3c59e1a6ff9db4b47f37d6aba3cd58c7d0812728f99fca4ef4a76ac6ca6b39b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7021486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:870a7934015f2fdd95171c9b09eba4fa97f9fde042a5e5d975a6dd376f75765a`

```dockerfile
```

-	Layers:
	-	`sha256:465d17598c0f7fdd0a5c9f68b9bcb3132637e77f1ddb6e267c4a69f1b10f1e4a`  
		Last Modified: Tue, 02 Jul 2024 09:33:54 GMT  
		Size: 7.0 MB (7005512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df45b66314009052b48161c3adcb1cde720f2967d79d464325ba41638dbd27c6`  
		Last Modified: Tue, 02 Jul 2024 09:33:54 GMT  
		Size: 16.0 KB (15974 bytes)  
		MIME: application/vnd.in-toto+json
