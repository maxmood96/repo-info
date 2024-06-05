## `clojure:temurin-21-tools-deps-1.11.3.1456-bullseye`

```console
$ docker pull clojure@sha256:4161504f34fa1aa96b2c97928c1bdafee00175d46e3fee31cee95bb294fedcae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.11.3.1456-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:af359011dbcd960ee36b7b27c54b923313eaf90829dbb1594d1ddffd99ff8de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.4 MB (282413944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e94972c3a7d276b6372c9c803eac1724843203ac30b41584f4d490664ae9d717`
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
	-	`sha256:0be3345c005b31e46e702bbb41d8392b21f4fd92cfd1be18ec02e83935095ac4`  
		Last Modified: Wed, 05 Jun 2024 06:10:33 GMT  
		Size: 158.5 MB (158497970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4395dbfe4aa9eb14543eba1a325b6323f7f72361312c94be58cdd2d644e3ef6`  
		Last Modified: Wed, 05 Jun 2024 06:10:32 GMT  
		Size: 68.8 MB (68815527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5c301e29f08a2864c59fe59bcabeedce21e5764439f5753826613fdfc08498`  
		Last Modified: Wed, 05 Jun 2024 06:10:31 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b69b4c9becf3bf5a40359dc381e01533e42413f96a1bf12d2a65cb5a74ef01d`  
		Last Modified: Wed, 05 Jun 2024 06:10:31 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.11.3.1456-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:9b8f09b5e7ab0651cd59cb4fe00226164a1135a8dc92bde23ab4df75398adcab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7016503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb2d8a7e203e5e9c874cdf437d70a1b8694a87d1b507a30e2757c5e9790eec2a`

```dockerfile
```

-	Layers:
	-	`sha256:924c8a5a5138ea31bec1452c036a5110e68c1f412210a34e59ae55e24d24cd66`  
		Last Modified: Wed, 05 Jun 2024 06:10:31 GMT  
		Size: 7.0 MB (7000437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72549129c4e2d50956f209aab544952364b819e8675e61e2e52e86bd9b4c5f79`  
		Last Modified: Wed, 05 Jun 2024 06:10:30 GMT  
		Size: 16.1 KB (16066 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.11.3.1456-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6fa4f91fbbadd4a04fa12efc01a82884af59d8b6373c2c5ab0a8a42c3b4ddba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.3 MB (279334751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fc539443809d7e35e54af2764a062b6fdacef5f4ec3d90a1c9638ada2cf1ed`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:47 GMT
ADD file:43721c605da3f74f0c3f71384780fc0e57e2478b88197672caaf4baa3eddab23 in / 
# Tue, 14 May 2024 00:39:48 GMT
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
	-	`sha256:078d9526cc72763b2db16388f6b511c18a73e3e7f9d229364b3b85a6b5277bc8`  
		Last Modified: Tue, 14 May 2024 00:43:13 GMT  
		Size: 53.7 MB (53738990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc049db95631c97c1bda8b762a6f7f5c13f1c41234437eb694b8f95ec2dfb27`  
		Last Modified: Wed, 05 Jun 2024 14:13:27 GMT  
		Size: 156.7 MB (156665634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfc50fd97ac46f2cdad1c11ca2dfdbcb80683999776e02d485a2de1d9b91100`  
		Last Modified: Wed, 05 Jun 2024 14:17:17 GMT  
		Size: 68.9 MB (68929080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b42172985cb8feeaef96235e1d3e082023124adeb901518892463af54de4a1e`  
		Last Modified: Wed, 05 Jun 2024 14:17:14 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24db6c1280a437d44778a7f9207e5864f829ca11c631df05eb0dded71228a1d1`  
		Last Modified: Wed, 05 Jun 2024 14:17:14 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.11.3.1456-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:ecfa2fae9bbf758b28f7abe0154a70d4bca237384db3c04dd1279ae9399b0b5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7022809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d73ca7e2a0b22b0da12724112d955a87b0d6a060ddda283e70598546ce0229e`

```dockerfile
```

-	Layers:
	-	`sha256:3a34b6f42e3e95d2f68603e619933e1dcdff29738ac5ab3ef39c2e3ca69fb90d`  
		Last Modified: Wed, 05 Jun 2024 14:17:18 GMT  
		Size: 7.0 MB (7006183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b19b87a7842ec88983e480a9edd13347e5fc9afa3925797679e0a1648936e3f7`  
		Last Modified: Wed, 05 Jun 2024 14:17:14 GMT  
		Size: 16.6 KB (16626 bytes)  
		MIME: application/vnd.in-toto+json
