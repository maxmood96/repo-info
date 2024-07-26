## `clojure:temurin-21-tools-deps-1.11.3.1456-bookworm-slim`

```console
$ docker pull clojure@sha256:898cf9a6bd5df0aa6300ad84ecc9a7e8a120ff30ecbb0e37fd06721411b9ed89
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.11.3.1456-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:16bd2561ee9cc358993f4e5c0321f6241caec7461d3848ab6a5fb18c09dbd556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.8 MB (256773984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce4c41402a3d4181adb4e7fefb26d69d1057b7b08d7742e8c41a222aad36926`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98dbfdcf76e4e1c0b8d89142f40d6fee17d473316dfd78d9e816491a5bb20234`  
		Last Modified: Thu, 25 Jul 2024 19:05:27 GMT  
		Size: 158.6 MB (158579324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b35d44bb3505e7a4dc8297a30f0543caa3801b1647b2107eb11453028a7d32`  
		Last Modified: Thu, 25 Jul 2024 19:05:25 GMT  
		Size: 69.1 MB (69067333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac459e25aea6b1f7852f14609effff5531eb3fe3431aa5567d458947129e6d4`  
		Last Modified: Thu, 25 Jul 2024 19:05:24 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdbdbd3aa44406aff68e5097a3c48e12074c8ad093b6f99c6eb7e18e62e9ba61`  
		Last Modified: Thu, 25 Jul 2024 19:05:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.11.3.1456-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7f575ac8d3659430b7e31f846a4c30cb6a141efda003929481090f94e081813a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4762079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d6a471d9645f112f63ac8a570e4d08249287976189fb91d67b4d8f4503a0bae`

```dockerfile
```

-	Layers:
	-	`sha256:037be136b487ff0cf3abfc0f16a033d347d00c023690693826d7d3f4cbadfbd5`  
		Last Modified: Thu, 25 Jul 2024 19:05:24 GMT  
		Size: 4.7 MB (4745870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a28dc3dfab4eba0b0d6ece7c9a9078db574cb2cb37ba335cd484328d4d86b0fc`  
		Last Modified: Thu, 25 Jul 2024 19:05:24 GMT  
		Size: 16.2 KB (16209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.11.3.1456-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cff8ed7f22a58333f1238b5300af58ffb0953020e00e82afa38b94cebb502c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.7 MB (254721796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85dc8e7bc0e2d8955e6537f114b243b220867e13c479a364f8d212a106245c3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:51 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Tue, 23 Jul 2024 04:17:52 GMT
CMD ["bash"]
# Thu, 25 Jul 2024 20:19:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jul 2024 20:19:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jul 2024 20:19:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jul 2024 20:19:09 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Thu, 25 Jul 2024 20:19:09 GMT
WORKDIR /tmp
# Thu, 25 Jul 2024 20:19:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 25 Jul 2024 20:19:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 25 Jul 2024 20:19:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 25 Jul 2024 20:19:09 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 25 Jul 2024 20:19:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc886ce209c192998c2b3f4ed4247246a0d7842bf3146abd8f602bc2fac044b9`  
		Last Modified: Thu, 25 Jul 2024 19:40:41 GMT  
		Size: 156.7 MB (156746213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12fae6f41a4c1f4af460736446307be384dffad863693871feba735cc153a721`  
		Last Modified: Thu, 25 Jul 2024 21:23:06 GMT  
		Size: 68.8 MB (68817970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641efdfafcc21905216739b43aaec73dbd1698fb1ba73e8543a66af24cc733af`  
		Last Modified: Thu, 25 Jul 2024 21:23:03 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2168dbdaadafcfa572e4947561067fee1a8167bb29ce783f6b98b5865de6ac4`  
		Last Modified: Thu, 25 Jul 2024 21:23:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.11.3.1456-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:44fa4ccd50c4d3c63b61a7e16f79a9e9f3a7885a10ed247c86bd1bfe4a3a25f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4769053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee353f961861114f732d5996346cef6029df0e4f015dac0f4b5f09016d70d40`

```dockerfile
```

-	Layers:
	-	`sha256:a300e95d472f0d9da62b20ec4128c77b873c780be1c23729eeed9b11a90f6ef3`  
		Last Modified: Thu, 25 Jul 2024 21:23:03 GMT  
		Size: 4.8 MB (4752279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c98fe0e7d4f1b7e9728087905560520b591f9079b0bd52cf905734348169d324`  
		Last Modified: Thu, 25 Jul 2024 21:23:03 GMT  
		Size: 16.8 KB (16774 bytes)  
		MIME: application/vnd.in-toto+json
