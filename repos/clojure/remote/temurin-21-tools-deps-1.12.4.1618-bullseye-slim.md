## `clojure:temurin-21-tools-deps-1.12.4.1618-bullseye-slim`

```console
$ docker pull clojure@sha256:59ddc89c171f1fa1eafebe541b5915ed153d3df7dd37276cf04b2a9b12765986
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.4.1618-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:399a5a3f48e97077f07d8b7c52f041cb99855f382b521e479cabf51ffab686a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.3 MB (247299463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eedffd3e9dd7a160533a818acc37d5bbeebbb8f69b2fd61296995b71665d423`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 03:16:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:16:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:16:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:16:16 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:16:16 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:16:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:16:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:16:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:16:31 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:16:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3da7ff29e52d22e60f513eee4cfd7699bfccfb9057da6f1c79a50b44f80437`  
		Last Modified: Tue, 07 Apr 2026 03:16:54 GMT  
		Size: 157.9 MB (157857052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2550881202896a08462e0a482f270eabd58cdea51208be092b0f14c8a2ed5e`  
		Last Modified: Tue, 07 Apr 2026 03:16:53 GMT  
		Size: 59.2 MB (59183348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcdbbb369c36ad3fd2e6e668b0bf25fef94178116f1b24f37cc2191ffded714`  
		Last Modified: Tue, 07 Apr 2026 03:16:50 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b292164a587326ff930f4b7f6046945f7986e0b1eb051385bb018583b5da02`  
		Last Modified: Tue, 07 Apr 2026 03:16:50 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2ae7da1636cb6006a66e8d3d9b658cd5a63bb87189c63c2fa13f45c589598984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5337741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14569d429859a246b3d613fa1bced6bad6b5662244ec55996ad33bf456d58def`

```dockerfile
```

-	Layers:
	-	`sha256:958f67758939e39f0a7f812b4ec5bd5500ee26c07ede857cb54c0f32b934bc9c`  
		Last Modified: Tue, 07 Apr 2026 03:16:50 GMT  
		Size: 5.3 MB (5321905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3c688e2e5247841074e70c7be7cb18c3551cd588a4ae0976b9c8f573175a077`  
		Last Modified: Tue, 07 Apr 2026 03:16:50 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:608f92784c6ddbba3d9924c93d0eaeffb2275b5333ec0a70c960c89e2712c45d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244202477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13f816455248bfc5f1d84249c72e1d8d73ffc1ab462bb9c567989e449bf8d0a6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 03:26:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:26:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:26:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:26:54 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:26:54 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:27:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:27:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:27:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:27:08 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:27:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662db87eb8c9c099fa996f98f4061d517bbd5dd471c0da52aa51de2c6d5746f2`  
		Last Modified: Tue, 07 Apr 2026 03:27:31 GMT  
		Size: 156.1 MB (156133049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a64e8e0f3e5d8adec204102854db8960e2c1a276a4f10eaf9f8c080e9c6de3`  
		Last Modified: Tue, 07 Apr 2026 03:27:29 GMT  
		Size: 59.3 MB (59323699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f25dd7c7c3edaf45d4df452512ba5d4d48339ebebfcec4c3a2ee8d891f2b178`  
		Last Modified: Tue, 07 Apr 2026 03:27:27 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6513c8a86619a58443a5efb5b7ad8808d5f74df02343adc6c415882ce5298e4a`  
		Last Modified: Tue, 07 Apr 2026 03:27:27 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9e35ea43d7d60e0e0c108177cf43fc787207de2c22490fb01001a8f8cf0869f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5343591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:188014cb9958a1f24efa21e084ce6069ed1a853dc405cb2a913179600bd68a6f`

```dockerfile
```

-	Layers:
	-	`sha256:1dad5411b66f68927be285799317be0c1e55194434cba98ea7a740c507fd4f6d`  
		Last Modified: Tue, 07 Apr 2026 03:27:27 GMT  
		Size: 5.3 MB (5327637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1962dd68f4c6c4fca5199c46011f789a838bab07a8551b217ffac3d9f123e957`  
		Last Modified: Tue, 07 Apr 2026 03:27:27 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json
