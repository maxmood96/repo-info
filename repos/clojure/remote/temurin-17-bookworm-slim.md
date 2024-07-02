## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:42c7081bcea1b1523fba444fec96f1ddcf0b25fee44d48b37df304a10f4695da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:998e97e991d94cdc6fa169d0ba888df1314f101702b139590f2ed11da7e35ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243288956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bad223f10ec1633796c7b1d148c0ac001b0fbe25272d452d591646dcba15782`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd4aed23fd1b7814575cb5c4ed9f603fa21cdc30396915a7b20403b058a802b`  
		Last Modified: Tue, 02 Jul 2024 07:07:17 GMT  
		Size: 145.1 MB (145095124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2afdd3ad080282efe934394621080cff91fe1ab76354abb9ef69af88908c8d1`  
		Last Modified: Tue, 02 Jul 2024 07:07:15 GMT  
		Size: 69.1 MB (69066512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27706f8abfc9d9f67753cea5bc15975f4267f0877a566f008b2650387982e40`  
		Last Modified: Tue, 02 Jul 2024 07:07:13 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5130eb53ad9ec6610e7491d63b0b86a6767f603b8cb9335df9ffb7b264a35a6d`  
		Last Modified: Tue, 02 Jul 2024 07:07:13 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:aabe2000a7c5bc90efe53b325651514d5668dfea4e94142eaabac8504d10a3bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4720551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c2822ec103313db8936f6077d6be1424a4b3e7adbd4208609782feae3ef597`

```dockerfile
```

-	Layers:
	-	`sha256:25a0369ba62ea1a93f5a226a07b20f7447ac20f53584f12848397e6f456a8fd0`  
		Last Modified: Tue, 02 Jul 2024 07:07:14 GMT  
		Size: 4.7 MB (4705039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dec31230197b784b2768fca8ba0706181320711b49695a7a9a30c4d3a30474a`  
		Last Modified: Tue, 02 Jul 2024 07:07:13 GMT  
		Size: 15.5 KB (15512 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1813506480129d1584d5aac76644ba3be29df3561ad841ef23392c0644a3fe0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241868447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d960cdd17e197f3e665f11efcad0de13e47ba38fa66c9c169dc6098f8d7faf1a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dadd56e10669dccfda0942b5194b9b287f0ec0f4e485936b0b75a7a4a1d3153f`  
		Last Modified: Tue, 02 Jul 2024 09:28:46 GMT  
		Size: 143.9 MB (143892757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b00702892ae8dcd1b799047eda04eb96ebe81182c24fd0e71fd61b138b7669`  
		Last Modified: Tue, 02 Jul 2024 09:33:10 GMT  
		Size: 68.8 MB (68818087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9c47b86e48887b51576006f8b33d0537a2b229f3d9cca3a58f7e64f406b0bc`  
		Last Modified: Tue, 02 Jul 2024 09:33:08 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56639b5cf3609f79953d913621ea4785c882e4f3b1b211d9b915d49894d4fab9`  
		Last Modified: Tue, 02 Jul 2024 09:33:08 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7b99e315e0b98e3e14f08441767d723abf674cff6ea3210c86dce92806adedcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4727477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cde0b5e5b47f21b1fdc476a770bd51ba6259ef4f4b5b55899e9661fa89e0f06`

```dockerfile
```

-	Layers:
	-	`sha256:d9cb985b481410840e959794bd36f74a581e130d5873e38fefc629aa64609421`  
		Last Modified: Tue, 02 Jul 2024 09:33:09 GMT  
		Size: 4.7 MB (4711424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee000b2c4035d3f161bf4a6472db5da1803830471d4c50aaa50654068af09a65`  
		Last Modified: Tue, 02 Jul 2024 09:33:08 GMT  
		Size: 16.1 KB (16053 bytes)  
		MIME: application/vnd.in-toto+json
