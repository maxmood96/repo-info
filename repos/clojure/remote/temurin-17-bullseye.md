## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:b11cadae45cdd61e74dc5fc86ab50990165d969b38d122ef148fe2b95f633331
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
$ docker pull clojure@sha256:8716c101282bdcb1a28706674d3d318eac76c8b3ea22143310e35e30eb21eb54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268868697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9f042f3e8cc1f6ba48dbd14b4b40c7fa412594dffc62a17855eb9da90517541`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
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
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01fd8eeb34c0247192f41a369c730aae5578466a11bc121862b4c34cd3091d0c`  
		Last Modified: Thu, 24 Oct 2024 09:16:11 GMT  
		Size: 143.4 MB (143360986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c2ad3a8a6963122900c08a6de827dc5b2bb83e2f7b1a01a42f17659a19ed60`  
		Last Modified: Thu, 24 Oct 2024 09:21:23 GMT  
		Size: 71.8 MB (71771775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c1f7ec0d3abff92586fe5307e2314cd5f1567bfdb9af6a10b8b68768447098`  
		Last Modified: Thu, 24 Oct 2024 09:21:21 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d65d818718823a95071491fdfd87b86c1bfa160dfece0fca5f4e9a7d5058ba`  
		Last Modified: Thu, 24 Oct 2024 09:21:21 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a82ea7399d9f32fec0761e14dc532a76268766782437525eb347db00ea2c22b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7236695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a87bb2cb8c3732427efdf0139b59cff03060aa935c65766240c63404f955af0d`

```dockerfile
```

-	Layers:
	-	`sha256:95a668e6895673e6e890ec09b6347b8f9f99d61f3ebabc0192e8cb653cd26c46`  
		Last Modified: Thu, 24 Oct 2024 09:21:21 GMT  
		Size: 7.2 MB (7220937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e8f9f470923055c15a1d9fd3cc7e64ffffbbf77390bf69845a280b48768fe38`  
		Last Modified: Thu, 24 Oct 2024 09:21:21 GMT  
		Size: 15.8 KB (15758 bytes)  
		MIME: application/vnd.in-toto+json
