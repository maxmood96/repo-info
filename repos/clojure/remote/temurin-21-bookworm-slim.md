## `clojure:temurin-21-bookworm-slim`

```console
$ docker pull clojure@sha256:e46b2e43c5a347cc4103a8e71f0137a0e7551c9d11cb530a842cfd3ddcf3a581
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e3399ca9e9db5f984e5db4d21bfec39e337da82d3ec6232630ab4186ee9242c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.2 MB (257189592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4b82fa28fbe3d2cbec1f57153e984e0b70273a6f725eeabbe942cc86f7e899`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 06 Sep 2024 16:59:26 GMT
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
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d239d93d81e78fcf7292d1df50807930fd680355fef94ffef3c2c6c2242b17`  
		Last Modified: Fri, 27 Sep 2024 06:01:22 GMT  
		Size: 158.6 MB (158579307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f619b0bf094588bf8812d45503982060ab16ec41cf7b4f6a80ba7b01d114aa96`  
		Last Modified: Fri, 27 Sep 2024 06:01:22 GMT  
		Size: 69.5 MB (69482972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5649c458d2d4377b85c28a9ddbeceaed20cecb1dcff13fa0fb9c616e2b455811`  
		Last Modified: Fri, 27 Sep 2024 06:01:20 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd97c9b74394a210843772cef8f61e1745430869b3dfe27145495c0bf20c185`  
		Last Modified: Fri, 27 Sep 2024 06:01:20 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1cafbb524e27bbc171f208b291b1b19dcd457ab7ef2a988317b65c2c033fe363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4914857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14bb59b6b1b9d0099c164097a8cdb06726e65d841d0bf2d5b5b92af4fac64453`

```dockerfile
```

-	Layers:
	-	`sha256:72d0a60694354bb387816822cdf83a5adb2d1fef9858e523b82f34f7569f2e1a`  
		Last Modified: Fri, 27 Sep 2024 06:01:20 GMT  
		Size: 4.9 MB (4898648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b87de6336d21b141171518b810054c1ffe2f48fdafe6bdc69ad11305cd67d24`  
		Last Modified: Fri, 27 Sep 2024 06:01:20 GMT  
		Size: 16.2 KB (16209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2e914c1310fb9948d548c3f766baed5c55e28d788f40b0dd7319a3b8fd45151c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.2 MB (255248851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0208c365af895b97bbc3ffb1e73919cd11ecb932f0bb23e1ea4c363663d591e2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 06 Sep 2024 16:59:26 GMT
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
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856625ad0308646fed5ac9c4f563bde32bd5fba6c72fee437ea487f52cccb6e2`  
		Last Modified: Fri, 27 Sep 2024 10:40:13 GMT  
		Size: 156.7 MB (156746168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1911179e75916a0e7d09c01a2050b922e70164719febac4924750df519b92a`  
		Last Modified: Fri, 27 Sep 2024 10:43:55 GMT  
		Size: 69.3 MB (69345277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4f5c4b8e8849c6cd61de7d0879d20977068f98dd7cdefb005932971470cde2`  
		Last Modified: Fri, 27 Sep 2024 10:43:53 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a665863e986e457642f715a084a50292d32a999c2e546958a366f567a7ef1ab`  
		Last Modified: Fri, 27 Sep 2024 10:43:53 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c162015016c28a15e909e06c6b357ddba57212423ceb209c9a6ea268357dad2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4921212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da91d4d47aff6036010e53a79bedf134cfa73316a85e7687d8f7ce4543ffff28`

```dockerfile
```

-	Layers:
	-	`sha256:b5032ba651e175dd1ee31408b00fd6d5acdbbb41b91c4aa71a10cf6e7b84f8a0`  
		Last Modified: Fri, 27 Sep 2024 10:43:53 GMT  
		Size: 4.9 MB (4904438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:799ae697e4258a60bb4f1e873c9b9ccb9842801fbf3c1d12202d892b7eff1131`  
		Last Modified: Fri, 27 Sep 2024 10:43:53 GMT  
		Size: 16.8 KB (16774 bytes)  
		MIME: application/vnd.in-toto+json
