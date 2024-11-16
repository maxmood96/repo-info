## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:07fa2856f8ca7bdbba474d013089f87de37978c330f257c4fa3a4cf51f6de334
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:a0ec96faa5fa3cd1c118ca4e0f8c14ef1fa2dd13ba3b07fce48b2fcb920d92dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.1 MB (275051414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d527ee724cf5f97b89fcede4fe47bdcfc6fcc502d043ffd1794aea837925e657`
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
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94461e3ae2b8b38fe1abb59368060918b007f1d298feddebe49cd5eacf83fa2`  
		Last Modified: Sat, 16 Nov 2024 04:50:14 GMT  
		Size: 144.5 MB (144536720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c89e36d797256a891ce15435b2f9e41412345e510772fefca0d644b40ac2008`  
		Last Modified: Sat, 16 Nov 2024 04:50:13 GMT  
		Size: 80.9 MB (80937960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f865c53246b005b14f85208c22414bfad6bbecba561804d71b9d73de707cd25`  
		Last Modified: Sat, 16 Nov 2024 04:50:12 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b84eb3057a68d67fa8015fd3d16829113cf8970ee44395568eb33b8117e4205`  
		Last Modified: Sat, 16 Nov 2024 04:50:12 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:6d5e04dec90f9e73637c8bd55b3312a33d6db92f8f598e32374553fb9daf5f0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7198244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dc454db28d9d8f4b2352fe04fb9c459fd1a86bdf118fe816930d0c820adace7`

```dockerfile
```

-	Layers:
	-	`sha256:237a3f1a7bbe884b402512c9efa8a3bcc92261b07a216313e861b7c63b3ada6f`  
		Last Modified: Sat, 16 Nov 2024 04:50:12 GMT  
		Size: 7.2 MB (7182423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:285f34d5e99bb55f30077d0a80b0d24a437e70e31c44d604265261e5e7067a8f`  
		Last Modified: Sat, 16 Nov 2024 04:50:12 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5aa1d5a176d82d3f5fe24d947db95a598b86d1ea7acc52ea0e9406728dd8ac55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.7 MB (273747613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0121e3e03db76f35df7c4814f931376365d19ced1223d2bc9aad2490fdb8101`
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
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4cdfadfff64b09387ddfd1934f0b9ac2ec91466224a631d4bad4e66c4be948`  
		Last Modified: Sat, 16 Nov 2024 05:28:56 GMT  
		Size: 143.4 MB (143360999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c54441c2dc522fb6d18172de1d839e8826085a8ddf681621c5c5e9a4ffdf7b9f`  
		Last Modified: Sat, 16 Nov 2024 05:33:37 GMT  
		Size: 80.8 MB (80798371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdd0b39f76afd6ae9674dff47c697ef3694387b807d729cf30118fcc3d9681f`  
		Last Modified: Sat, 16 Nov 2024 05:33:34 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def4a236bc4cfbe0169f7d72ab876a769afd14eb69c818cdcb6dbcabc4cd9df2`  
		Last Modified: Sat, 16 Nov 2024 05:33:34 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:304e46d72f0eec345df5aacf4368ed17e43429e54843ad7d45152bd965fcbd5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7204130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:117ff4674b001ff385c095cc4d29fef9e29ab6203cc7f63fa1885287acd30349`

```dockerfile
```

-	Layers:
	-	`sha256:01938a1b7c9569326859f489fced14d2c9b7f409afde6dff6bfaf78af7d66456`  
		Last Modified: Sat, 16 Nov 2024 05:33:35 GMT  
		Size: 7.2 MB (7188191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d2a94de31ef9ef48c2ff4813abd577d24ab336b9c750ae8a6f0e6ced7b1b83f`  
		Last Modified: Sat, 16 Nov 2024 05:33:34 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
