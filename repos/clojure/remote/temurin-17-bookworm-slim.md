## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:756d9c7757932b87e2de736c2bf5f6ac38837dc7be53bf43472c2ab43e28f549
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b020fc8d5dc1ae125cc0d0f67bbe6890b00c1b353030644bc5372d411c33517d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243776572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1ac85d9b26527dc666af238bdc94906f8a8b697c0c74b06aee4c222860f0db`
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
	-	`sha256:fe4e2c25d6821eeec21117ce3498aa4854a8b8756507316cf06c9ff7a8469ba0`  
		Last Modified: Wed, 02 Oct 2024 02:57:56 GMT  
		Size: 145.2 MB (145166509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ebd84c7a4da762f8bf2dc7124a6be263c824309abddbd62d668bb3814737eb`  
		Last Modified: Wed, 02 Oct 2024 02:57:53 GMT  
		Size: 69.5 MB (69482748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67ce5fd3ad004c7d5241100230c2bbb527963e59f95feb6ce7abce2a8bf8299`  
		Last Modified: Wed, 02 Oct 2024 02:57:51 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b347444537d904cd1cdbee92af385e06024ea03ef881d1eb72810ffd491e16`  
		Last Modified: Wed, 02 Oct 2024 02:57:50 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7e5d2dfbbb184c6b58dd570d4851f710f4d0c62e807929f1bca4efaeb8b5b0ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4909693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca38a5f4603d50b75ba6f4b404259598db6261bf9abd60dafdd103e9af7a66c1`

```dockerfile
```

-	Layers:
	-	`sha256:0c9d384250cb9db56e927ed8ba7759ae22ab4aac4a03800cd1a58af08c277f02`  
		Last Modified: Wed, 02 Oct 2024 02:57:51 GMT  
		Size: 4.9 MB (4894211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:172cdba2fdf493521b94b54bccaff2a5531d5aa741cf847279d9731c99b9a593`  
		Last Modified: Wed, 02 Oct 2024 02:57:50 GMT  
		Size: 15.5 KB (15482 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1425310093f112ae44f5bf99e93b83bf1d12298ca2ceb2b8aac15da88f9af7a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242462015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:260ad8ba3ebd196a5781a4ffec16df4ca11970d605ef01e247fe0e40d02caf23`
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
	-	`sha256:3a8ec743abe4864001d38c3b367b0e2a4fa8fd7fac75602b7803b3ee90e07119`  
		Last Modified: Wed, 02 Oct 2024 02:19:35 GMT  
		Size: 144.0 MB (143959484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb25aa09d5ab2c189f60050e5f926b304833b07cab78887dee05c12ab1925089`  
		Last Modified: Wed, 02 Oct 2024 02:23:05 GMT  
		Size: 69.3 MB (69345123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be09becd085327a30ebaa9c4ab373c71ff73d6905ca276332efcdcd143604fc6`  
		Last Modified: Wed, 02 Oct 2024 02:23:02 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6251e36479377cfc6795b259d43bb387adc79f705a17f4830afa351512a183b`  
		Last Modified: Wed, 02 Oct 2024 02:23:02 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e838caae7fc88e70b27c1bffa6a5d372b6fa4969258401069ed7f860412ac89a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4915601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3698aa3ceec6e3abf3497165fd1ceb45d762c82ab6a48b7c016046d960a923fd`

```dockerfile
```

-	Layers:
	-	`sha256:dd89c7cdbc58b3da0f1ca5d6587bced8ec163a6c0a76f8960d00b860f861103a`  
		Last Modified: Wed, 02 Oct 2024 02:23:03 GMT  
		Size: 4.9 MB (4899977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f40c3aedec7c1932f668e5875c30bb8c2818202f3d9cb3a25ef2b7d5f24a75c6`  
		Last Modified: Wed, 02 Oct 2024 02:23:02 GMT  
		Size: 15.6 KB (15624 bytes)  
		MIME: application/vnd.in-toto+json
