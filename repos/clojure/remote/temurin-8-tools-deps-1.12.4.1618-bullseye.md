## `clojure:temurin-8-tools-deps-1.12.4.1618-bullseye`

```console
$ docker pull clojure@sha256:cc9199e626c328e50908023ae4ca3d3b529bcc2703a749806c9d7d46e8a30371
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.4.1618-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:3e0680394cc740090064f10a865e83063ff1f2aca719a450e270e959cdb0c48e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178531864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d1d8dc3fbbbe95d435b389466ae1a98cb5c736d94ec35de3484dc97b6e1ed8`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:14:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:14:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:14:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:14:00 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:14:00 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:15:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:15:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:15:03 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1c662d8f6b122c4f09d6ae1b210df55a5ba6e7b529807c0757ccba0c1ac508e0`  
		Last Modified: Fri, 08 May 2026 18:23:06 GMT  
		Size: 53.8 MB (53763343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a158290ef3bc83a470b5c65c567ff0bb2a6cc3c6505b6cb8d3054500e1458a1c`  
		Last Modified: Fri, 08 May 2026 20:14:35 GMT  
		Size: 55.2 MB (55170111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab4a1575acfd46d67dda4989aaeda0894f8b2fce35446cf0a4d72f77e843088`  
		Last Modified: Fri, 08 May 2026 20:15:20 GMT  
		Size: 69.6 MB (69597765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7384763663190a91295631ccd6b4ea89ed787416a41bdabed208453c3c014d56`  
		Last Modified: Fri, 08 May 2026 20:15:17 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1618-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:dbbb60c87962f2fa390e75768cb617b6069b62506cd63756f9eca5851fa86023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7542034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4082d2f58374226121bab56f8bc97fffc76d41d85d9510de184290407654922a`

```dockerfile
```

-	Layers:
	-	`sha256:489fe5a0fde05117021f5beaed92027fc814080448df6f3beb2a2fdbdbb29e70`  
		Last Modified: Fri, 08 May 2026 20:15:18 GMT  
		Size: 7.5 MB (7528640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a612010ef61ccff494f64690543758487ff0e4bc47e9d0c4c0682c1fda41fff`  
		Last Modified: Fri, 08 May 2026 20:15:17 GMT  
		Size: 13.4 KB (13394 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1618-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:66fa8fa1df58ac7cf6a65ef8c64adbc591110269c301cecdca2f1fd1b282b354
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176244585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea938c331e4ab689ee5bb2acbd1f727df5820a5ad558bd66ea00c0ecb78d765`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:18:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:18:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:18:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:18:34 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:18:34 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:19:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:19:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:19:27 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12b6a467874998b3612540bb45c100aae35859e4af5e3a1e3a16ae05257de53`  
		Last Modified: Fri, 08 May 2026 20:19:07 GMT  
		Size: 54.3 MB (54251616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122f5fbb7fb94a39810f68a6c50576fb5b57e322702b23287f4228ccf977cdd4`  
		Last Modified: Fri, 08 May 2026 20:19:43 GMT  
		Size: 69.7 MB (69739113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31b8c1e51e8ec943d55f1693add2ecc3176073b60492e661123b05e1aebd385`  
		Last Modified: Fri, 08 May 2026 20:19:42 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1618-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1f519c08a50c5228b7f83733c7c7afd36b54742bfdd009d99cb3e9cb8991f5a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7548751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f299d863f5e70df5963bd25b83f421be9bbc74c634bfffdf0b2ae16c13cb4f64`

```dockerfile
```

-	Layers:
	-	`sha256:fbc610c8e5fcdb5305713310151f1c7562df2b16a40ffad036dd3775ccdc9e17`  
		Last Modified: Fri, 08 May 2026 20:19:42 GMT  
		Size: 7.5 MB (7534439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9deb6128d0405925b0566cd0bf5f1ea8b389f9e119a6051fb00022d983ace17`  
		Last Modified: Fri, 08 May 2026 20:19:41 GMT  
		Size: 14.3 KB (14312 bytes)  
		MIME: application/vnd.in-toto+json
