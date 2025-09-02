## `clojure:temurin-21-tools-deps-1.12.2.1565-bullseye-slim`

```console
$ docker pull clojure@sha256:fc36f7e892fb24f0692a0757de7af7d63d9a8e330c4c183725be1fc2ba01b9df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.2.1565-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:966b194da0f7a4259d379d3f2aa4bbcadadf5a69e9772c5403142391ddeb78f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247212869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5613b8b9d8e9ebc134a9b42a02eafbcf6779e393e1e4badb739c9ec2d1b5b45`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3e41ca17193bcd7630e4dd210602930b1f94464bdd59680bbf6654206f7707b8`  
		Last Modified: Tue, 12 Aug 2025 20:44:40 GMT  
		Size: 30.3 MB (30256118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff7453025b07d79c590fcb9a84b20e56641295fe36729ccc2c105d4313bb769`  
		Last Modified: Tue, 02 Sep 2025 04:30:43 GMT  
		Size: 157.8 MB (157804819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a44bc22bf6836ecb0146e097a74775724409bb082f938b602c5f44d498fbc42d`  
		Last Modified: Tue, 02 Sep 2025 01:31:51 GMT  
		Size: 59.2 MB (59150888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0c21caa9969bca4e5e0d797e71c4898256c1ddf47ccf3085b8af065da417ba`  
		Last Modified: Tue, 02 Sep 2025 01:00:59 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1230c2ab03337100f4878e30ec655a037decf027baf6700b2ab2c94da2d2c85`  
		Last Modified: Tue, 02 Sep 2025 01:00:59 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.2.1565-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:afedd7c0e682c85c39ab83dd5473377578d9a354d8d037b0e6b5a5f35843339b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5328440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3bbb5eba1495ad0c16325b2219f0330c1c0771b7efcb9536a78740da18e9fc`

```dockerfile
```

-	Layers:
	-	`sha256:8115a49d7ef25770f68d45a2086cc896403bdbb2afd2921def1c7ceff3a7b74d`  
		Last Modified: Tue, 02 Sep 2025 03:41:04 GMT  
		Size: 5.3 MB (5311865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fb45f8c7c16b49adf2df02f5e521fd54f9020f8ddc0bf796cdd41eb0e816602`  
		Last Modified: Tue, 02 Sep 2025 03:41:05 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.2.1565-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ebbf0fafcc6a26ced2f86466a7b2c01b29a8c5122b9d71fbd3a47fc0afa7c2d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244115463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7734e53e4822658322c24d1e1731d94574a50ff15dfa4063c4afeae60b0f80a8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b99ef417bc3eb3946e7b3162f6c19dbca1039f3b4124deb116c3a0ab763e65ad`  
		Last Modified: Tue, 12 Aug 2025 22:33:30 GMT  
		Size: 28.8 MB (28750491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2018a747c37989de117c5255ed9b90797d04cc50b7b51efd380710484b6be5df`  
		Last Modified: Tue, 19 Aug 2025 02:32:37 GMT  
		Size: 156.1 MB (156081251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e668e191be6b5e37eaa898607d9debab8e85d1b035855ad75ac9eacdac7d617`  
		Last Modified: Tue, 26 Aug 2025 19:11:17 GMT  
		Size: 59.3 MB (59282677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a2cc1bac12b875dc377b696885dc6189c6ad18649b1a9b98c6ade0deb5c2b9`  
		Last Modified: Tue, 26 Aug 2025 18:39:44 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c351be3ba21ff9a183bfe9bd126247ac7c54d3ac051e3f7e2013e8c0647153`  
		Last Modified: Tue, 26 Aug 2025 18:39:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.2.1565-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:80f009ec6e61e47891eb07f87f91b5d7365307026444f792663199e885ff57dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5334337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ba8c476a9ea97c1ad74925fb83cf9442b233410315ff270bb8c9321cff4fa25`

```dockerfile
```

-	Layers:
	-	`sha256:7a42fd7e3c49db0255acbf699b5caf4ca7ddf222f5596e983a109c6f4158967d`  
		Last Modified: Tue, 26 Aug 2025 18:40:16 GMT  
		Size: 5.3 MB (5317621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b914be260355af98554f2a206fde68ba5e204ce9f375faf21d032be536b936c`  
		Last Modified: Tue, 26 Aug 2025 18:40:17 GMT  
		Size: 16.7 KB (16716 bytes)  
		MIME: application/vnd.in-toto+json
