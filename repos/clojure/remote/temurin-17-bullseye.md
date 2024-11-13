## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:53f2e233919889c4493cd59883806b2406bcfc7272a5fa2fd8df4d089a5a1b26
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:cd4bf14dba713ff0bc47f6f58d9f53bbebd6d04c7217b3fae7259cf7f362b5ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268783709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a53408911e4bc93f05a4965b92e725cb970ef1902ebc65b72cf29cb583969a1c`
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
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc8726315d8511e8ba1a7645bae8b72589d92fa37358f13733b20279b1bd37fc`  
		Last Modified: Tue, 12 Nov 2024 02:24:06 GMT  
		Size: 144.5 MB (144534759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea83650d235b9b84e3509af6adb1af959713291e879afbf36535c078ae1d9d9`  
		Last Modified: Tue, 12 Nov 2024 02:24:05 GMT  
		Size: 69.1 MB (69139129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c269fba99635e5dbfca4ccf8dd46adcff344b2dc5f4c9bee9bac14dda3dea5`  
		Last Modified: Tue, 12 Nov 2024 02:24:04 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d30f17de202f76fb0fae677e6d1a2ea8c77f6154b6dea68ebd74260bbd4684`  
		Last Modified: Tue, 12 Nov 2024 02:24:04 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:03cb285b195b7d43a2f2c470533d86dfcf28f2c630e24ea2da130b8d6dc846de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7231690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c73323ff21956365cd8299456054520f5edc01b3dbcf8d52e3b2bdf8aa69d2d2`

```dockerfile
```

-	Layers:
	-	`sha256:555ff1b61db69a71549bb93520e561f76baa6847b5310791eef3c5e16406b62f`  
		Last Modified: Tue, 12 Nov 2024 02:24:04 GMT  
		Size: 7.2 MB (7215870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:042fd80b95ea0a0bcd52e6f0ebe078a7297abfc4cd5ce51bf2cf947ade4abfa7`  
		Last Modified: Tue, 12 Nov 2024 02:24:04 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b8a83ebf3aafab220ce4e1542176d742d66264d23a4840df6ed4e02b6e560522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266396784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e39b93e12066ab104a04934e260ea6efc870f34ed365e7e97156fb2b6032c5`
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
	-	`sha256:a839664fe62f615da74af799f94ccbc890a15d0f78470aac54302c2fd5475615`  
		Last Modified: Tue, 12 Nov 2024 00:57:41 GMT  
		Size: 53.8 MB (53757072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d15249eff07538c027628521f52137c234c529061f8ce1083ea87c97014f2d`  
		Last Modified: Wed, 13 Nov 2024 01:19:46 GMT  
		Size: 143.4 MB (143361011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98cca84c0b92a4170f90e11f8d31ae99676336a779a13eb733c8240252f6deee`  
		Last Modified: Wed, 13 Nov 2024 01:23:32 GMT  
		Size: 69.3 MB (69277663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647a30092c2071e4f394753d5777b3aef1a923fe872fe94daab8cb0bde90d866`  
		Last Modified: Wed, 13 Nov 2024 01:23:27 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4277a5cf90e17a2c303912a0e018ea21d5090fcd182c98180b8d8bed7f88797f`  
		Last Modified: Wed, 13 Nov 2024 01:23:27 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:6cc5ecad4e62b218a675bce18c5b3c7d30ce6ce2d39883ffe7ea74d797fe5a48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7236912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5ea57c1cfcaa0254d4a87b1d6eba795ca8fceca4626f50abe988f4b4e890657`

```dockerfile
```

-	Layers:
	-	`sha256:1b2f7d56f52cb2bce24e1c535ad36e71f74cdede60ff02042fb2b2ad936e7ddf`  
		Last Modified: Wed, 13 Nov 2024 01:23:28 GMT  
		Size: 7.2 MB (7220973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e8e19a4abdb45d727bb4a12b090dfbb62b4135823907b4c8bacedb3c71b8de3`  
		Last Modified: Wed, 13 Nov 2024 01:23:27 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
