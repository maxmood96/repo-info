## `clojure:temurin-23-bullseye-slim`

```console
$ docker pull clojure@sha256:72d55a6ce3ac54d1ea044f854da13ca2514adc0ad71eddaae6d90559a72c354d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ddf97e87af5b39495d88a59f265eeb88623e35a1cb3d2eb2db2b82647d9c445d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255487883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3deec11116b45dd502f2a2031aad728d5b3cf786df8baaeb4364591cb7d81c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6291cea46b602afd129310d494c55f346f02494c3e8b19474b50219fec417c4d`  
		Last Modified: Tue, 12 Nov 2024 02:50:43 GMT  
		Size: 165.3 MB (165295078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d99a5cd49a1cc5171f42c83d063dbbf18939dcfd4d923ef22a24fc6267a8781`  
		Last Modified: Tue, 12 Nov 2024 02:50:41 GMT  
		Size: 58.7 MB (58740208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0937d480891cced648bebb2aa849cfcde61145259dfea02dc7ebf39d7097fd`  
		Last Modified: Tue, 12 Nov 2024 02:50:40 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b59efa13a915d74fe2a867205a1127d53f6aa285f4ca45dfe85dea6fa1ebace`  
		Last Modified: Tue, 12 Nov 2024 02:50:40 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6f3c1e0f09f4b56abbda371fffcb117993c3e87133af350d25069ff65c10496f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5146243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:579174c8b259059bd29c0848881005fa56cb15d4a5be525f9324ee9e06381411`

```dockerfile
```

-	Layers:
	-	`sha256:b8d78d16e185c7dca68fd17934d5c1d0faf1804f0f8bbc3d2788e5c58f624d9e`  
		Last Modified: Tue, 12 Nov 2024 02:50:40 GMT  
		Size: 5.1 MB (5130365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2843b57954dd1b59292b1f4ffc25f11898e10f13e17362d2d5e376545769e6c5`  
		Last Modified: Tue, 12 Nov 2024 02:50:40 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d69357eaf9a58ec5bec3b308788893271331a896f392a3776ce6e1c6a5f25e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.7 MB (254655420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82477f6bf4b4e45303bb838d3b8460d23860fa5f66d6683be90f1f0c87a35a73`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c39ecb6761d88d6b99bc02593aa4cfc49106954164617203d5d1dc228b3fa4e`  
		Last Modified: Thu, 24 Oct 2024 09:40:25 GMT  
		Size: 163.3 MB (163281827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8c450b434e1e432a9d009d2a61f94487b28fc6c09e1490f99443d1386b33c5`  
		Last Modified: Thu, 24 Oct 2024 09:45:24 GMT  
		Size: 61.3 MB (61296799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbadada6858475dea503a936282d3a892bd6288bedf0ffb14e15629740ae3ea9`  
		Last Modified: Thu, 24 Oct 2024 09:45:22 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bebe4c206cf378ad26722be0d9a1ee83f3cc59205db4bca2f03bc6227dd6405`  
		Last Modified: Thu, 24 Oct 2024 09:45:22 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1bb286aa77ef7083ac5fb276aa08509afa6d95c72a06ae9ef26e88c36abce444
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5151274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eda4e45c71a38106e49cd736589aeecc10e3372b3ef920b1407ee1fca8b25e5a`

```dockerfile
```

-	Layers:
	-	`sha256:8d4b48200e51eb93df4bf580d0b9ef72981e6f2ac169d57c8d24847f88d004b1`  
		Last Modified: Thu, 24 Oct 2024 09:45:22 GMT  
		Size: 5.1 MB (5135444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75832dae156daac9d9d52a6e9068f8746fa321fe4d2ed8b9b0c575d0749f8d12`  
		Last Modified: Thu, 24 Oct 2024 09:45:22 GMT  
		Size: 15.8 KB (15830 bytes)  
		MIME: application/vnd.in-toto+json
