## `clojure:temurin-17-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:64796617574e580f31e9bf66418ecf54c64efb8c7ff040be159a19cba2dd5874
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:57ba3f807088e18dc7bc766cd3b2c469ebdc1c0c433c2f9e85500f69fcd89cf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.8 MB (267800561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c57ae8b1f21d345e6bd83a91730525c0dad7589b223d10a155371e8d243bc8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2d765646d883a37610a09973a079fbba4c7596e54d18d0447bdfff142389d1f7`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 53.8 MB (53754822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df56ff48c11fcb7b8faa42206871563e9e825c664b51ad4342fcb70420d672e`  
		Last Modified: Tue, 01 Jul 2025 17:35:55 GMT  
		Size: 144.6 MB (144635025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5392eff9247a1cd51018a57735a3fe0894aabfca08147f3b1cb1d838c5fed181`  
		Last Modified: Tue, 01 Jul 2025 02:39:56 GMT  
		Size: 69.4 MB (69409674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c163ecea565fc5eb2bcfb78f9f14cc6b41e1957bac0af0085e44d13f1e432ffd`  
		Last Modified: Tue, 01 Jul 2025 02:39:53 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63209d87677c10c14c0e00ccc6f20b2ffe0de0fbc39cbdb2a02bce284168d203`  
		Last Modified: Tue, 01 Jul 2025 02:39:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:342a2c71e7b08a56e93241c5248b2f41e6f7ad4befbee958e0831e78f65662a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7411459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7b4d3a5ba044ceb067c60c5e504e9284ae4e2e8e26164ba16a6880fdb399e9`

```dockerfile
```

-	Layers:
	-	`sha256:8c277b782cbfb43ab4b4972d5ef4d3918e8d53fe57f4979f6de36ccfcf3ea775`  
		Last Modified: Tue, 01 Jul 2025 06:37:04 GMT  
		Size: 7.4 MB (7395638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7626d1df349cc4b3394d0d7db3921faa7f8109f9f935449ff802caf3acc32e13`  
		Last Modified: Tue, 01 Jul 2025 06:37:05 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a0aeb0ecfd25d407c78835fa3d572ef55b050ab98bf7a8be6daec36b308072a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.3 MB (265303831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19c314a12eb1458ef35b65f64f4f99dc8225c15b35a7d590b8037d4ae7e79e09`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:df45b4853b6fce6b81d1ac6218d861c6d7c8c14da4be409d42ee4bfdf0737e71`  
		Last Modified: Tue, 01 Jul 2025 01:15:18 GMT  
		Size: 52.3 MB (52252254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feec1691bd8435b5a7725d0efcfdcabe177c8705d157d2f53c026cbb74e59770`  
		Last Modified: Tue, 01 Jul 2025 12:19:46 GMT  
		Size: 143.5 MB (143512634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce1d596abe46bdf7808ab5fba6467595b5fe6fa20bca14c88e66e204232ac4e`  
		Last Modified: Tue, 01 Jul 2025 12:25:14 GMT  
		Size: 69.5 MB (69537902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52d4e7b8ddd5e536ac32f68cc9fbf0f1d98a609d71c8b86aaaa767cafebb7a1`  
		Last Modified: Tue, 01 Jul 2025 12:25:08 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31bbf5ff5dd77152de5823b8fa53463efdbb8b09ae5d84545b9791478c6a9822`  
		Last Modified: Tue, 01 Jul 2025 12:25:08 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:981992332c56a66b6bbf4c5a51ef068b22cf1e9aa36f8b38c54307c22b6d6f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7416676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5050a6b6ec287f68b3a78f88c14d7cf33349eea3ac694076a210cd4d3de775a`

```dockerfile
```

-	Layers:
	-	`sha256:7f668aa44f9ea58417b430916cb8521d579b9aee785982ece7c0a29559e334ab`  
		Last Modified: Tue, 01 Jul 2025 15:36:46 GMT  
		Size: 7.4 MB (7400737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58c853e63a6a2c49b130b4e007a8fcdfc469d4427eecee488dbf41948977d19a`  
		Last Modified: Tue, 01 Jul 2025 15:36:47 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
