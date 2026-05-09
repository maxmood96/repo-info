## `clojure:temurin-21-tools-deps-1.12.4.1618-bullseye`

```console
$ docker pull clojure@sha256:09f39f46796cdd7c6c313baea012d54f022df5937f82fc890f3a8e5529944f41
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.4.1618-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:554f1c915fb19eb0d3dcdb8b1f309d712704a94d3513f136040edf9a529ffb84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 MB (281528679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e86956832275ff1c3765d781103b1c4566d0049cd35073fd4eaf934d5984d2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:18:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:18:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:18:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:18:28 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:18:28 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:18:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:18:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:18:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:18:41 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:18:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1c662d8f6b122c4f09d6ae1b210df55a5ba6e7b529807c0757ccba0c1ac508e0`  
		Last Modified: Fri, 08 May 2026 18:23:06 GMT  
		Size: 53.8 MB (53763343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4afd246b9ee127d1ec4b637884890d7bb2cd1175f5921292d913e73ef19adeb`  
		Last Modified: Fri, 08 May 2026 20:19:05 GMT  
		Size: 158.2 MB (158166922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676f63352f4ec8417ecfc2e9738c50c04c2e90f8b414f18c429835ef22b57cf0`  
		Last Modified: Fri, 08 May 2026 20:19:04 GMT  
		Size: 69.6 MB (69597371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8422243404a5ace1ba969b17533a4f2e439d89dc82e4c7d134331e00f6e40121`  
		Last Modified: Fri, 08 May 2026 20:19:00 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d527716af5bfef8c5dca7e5945e102b89929378ae164f3cfdc65e3d6848753aa`  
		Last Modified: Fri, 08 May 2026 20:19:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:748009d53195fa1615f6b8425dc5b44a3ed0e88ec623559e05bbd0e422e8bc83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7426064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de0992b280f96b8070daad6738565316d034e01747f4611aae434000ff55f0a0`

```dockerfile
```

-	Layers:
	-	`sha256:a91e235ccdc5ce03fb908f7df0123349b8f6bd1672df11cd812d022842c52985`  
		Last Modified: Fri, 08 May 2026 20:19:00 GMT  
		Size: 7.4 MB (7410132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dc04fe10316dd45ec7d4bd52fa306a010a976543ee24bb72b7a86663023ed1e`  
		Last Modified: Fri, 08 May 2026 20:18:59 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:62f21a721aedd5abc867b409079b758b1c9c37613d558360923fe3c839938be2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278454077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cf163047739d397386e5d8c1bd137199afba82fea088fa787289e5abf3a0cf7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:22:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:22:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:22:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:22:48 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:22:49 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:23:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:23:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:23:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:23:05 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:23:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fcc8b00d6a0c5e9d24791f79115e483541bddf8be70dcb616c763414ee390a6`  
		Last Modified: Fri, 08 May 2026 20:23:30 GMT  
		Size: 156.5 MB (156461190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054dde78bae34bb3e90e88ce6528341e82f83956a180f6e0464a6db1aa545ebf`  
		Last Modified: Fri, 08 May 2026 20:23:28 GMT  
		Size: 69.7 MB (69738639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b1695254e6122cdb69945d73e4665ab4e9236bd4930f4e9a919afee9429a1c`  
		Last Modified: Fri, 08 May 2026 20:23:25 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274289823fe1c5e411ca859285fa643ee2914d879a66c801cd4744d397bb74ba`  
		Last Modified: Fri, 08 May 2026 20:23:25 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:55a092aee8c77f6246adfdff3d9aafa8c2ddfeb7e006fe8152a90663eefca36a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7431281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65bebed4e6126ff37bf5316a89417a7810bc99437cd6533c4d8798db130c2a6f`

```dockerfile
```

-	Layers:
	-	`sha256:c3cccd1a025363b986d8d4e026194ebe8d2d5cd183c9ed983c109f3cc9ff9922`  
		Last Modified: Fri, 08 May 2026 20:23:25 GMT  
		Size: 7.4 MB (7415231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c034c56d94537bd3b27e6f107169acfb0bfe63fdaabc07b89aaa96854245b47`  
		Last Modified: Fri, 08 May 2026 20:23:24 GMT  
		Size: 16.1 KB (16050 bytes)  
		MIME: application/vnd.in-toto+json
