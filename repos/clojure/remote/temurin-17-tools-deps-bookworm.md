## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:de44d89b2d4a25e61b17a707a355b7a267f2aba57c5fa42117ffe41f0b84c5f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:db44f4604181a8a7d913d2877abe3d3bb93c0447a06bd0026fbcec5f3fbb23bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.8 MB (273779253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d3ee58326d5aef8d0699334f3f333f621bfcbd480f538f8ae833f3569238019`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6632396ef0a08ffe4b0540ef89c7c724dec17caf753123eb5ff78eaf38e7a0`  
		Last Modified: Tue, 03 Dec 2024 03:19:54 GMT  
		Size: 144.5 MB (144536676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26e0c85b478c728185beca6f4656ed8f9d4ce104e903910d33d394d521029f8`  
		Last Modified: Tue, 03 Dec 2024 03:19:54 GMT  
		Size: 80.7 MB (80744326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b9c819bf1b51ad08d227668122eb7519ed9409b6c8806cc8084d850fe4c18f`  
		Last Modified: Tue, 03 Dec 2024 03:19:52 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc7c92f678237d1a51d71f02ffe06251fab4cccd28be90b7ddf0589ba376b04`  
		Last Modified: Tue, 03 Dec 2024 03:19:52 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:51d01fdc1f7e88387e9764a3e0be21a96942f29a6cfeccb428f87414257a0c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7196996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cee9ae990a0cad00dc2a1c3a8ccd88a66ab3d0a31a50790eac99a5862036d91`

```dockerfile
```

-	Layers:
	-	`sha256:e1dd5417d7cc820f8d2abdbbe21ea16bd217ad000b1623716cf1115ca6f4eb7c`  
		Last Modified: Tue, 03 Dec 2024 03:19:53 GMT  
		Size: 7.2 MB (7181175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc8e6a2b93b1885e7bd0eb8e36c28927d2dc27b20bcc6552e58692bb794c3955`  
		Last Modified: Tue, 03 Dec 2024 03:19:52 GMT  
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
