## `clojure:temurin-21-tools-deps-1.12.2.1565-bookworm-slim`

```console
$ docker pull clojure@sha256:80c0f5b09b5f4091ab12f49ae88bd8a2dc6707c614026de0d30ff4e893f8c819
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.2.1565-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:22ce937f70117ed65ec2e3fe5be813c01e67e6af968ff71ae8fcf4066c232bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255703856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12921f23c33b918ca8141bd0a34df064f921a198364a4b108796a77967c11981`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772735cbc4e4eaf50d850a6da2342cabfd5da4f47277d47872233c0239c1235f`  
		Last Modified: Mon, 15 Sep 2025 23:27:32 GMT  
		Size: 157.8 MB (157804768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56708fc52ce18621db1d699dd69c0c987014689652c089fac6c01a750f5bec20`  
		Last Modified: Tue, 16 Sep 2025 00:32:02 GMT  
		Size: 69.7 MB (69669696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c12a6d9a3c7776d48dd242d685cd0633abaa6d981e4e5440cbfc4a677e689b`  
		Last Modified: Tue, 16 Sep 2025 00:31:52 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05466b4873593a2ce51cfc6d719887ce411cd76b8dcbb2d13105a05fce3dbff`  
		Last Modified: Tue, 16 Sep 2025 00:31:51 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.2.1565-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b3a226e087ca5619b4f7be31ca39d45d71f4fdc18dd3f81f110236a816511a65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5133761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a23dd8f6f7cf879597e1846b287de48c39b9cc0144ed1b3008d821a32bd7296`

```dockerfile
```

-	Layers:
	-	`sha256:feb710f18494d52a0052a4ed31708aaa3a567f2a199f5a78fe59f3108971abf6`  
		Last Modified: Tue, 16 Sep 2025 00:41:56 GMT  
		Size: 5.1 MB (5117186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4392de6b83eddbdc7f977cc05fad17a5e75c5ca9703386bf64c23a7d864272e3`  
		Last Modified: Tue, 16 Sep 2025 00:41:57 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.2.1565-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4182ae43ca095af11d6e00b816562f4b4165eb3ce9ab05125e8ab45866ce132b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 MB (253743820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc0c9bb6de50062980c4014f2548e5ee53d84f69238bc5ed15c22d801165019`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e016eb5233d05982762768220d793b3b22354fc424be95cc3cd5438eec264388`  
		Last Modified: Mon, 15 Sep 2025 23:27:54 GMT  
		Size: 156.1 MB (156081218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9551ceeb7e8d851b3d8d4685cb0e88c1d66982a447b1daef9600c4b35f30647`  
		Last Modified: Tue, 16 Sep 2025 00:21:58 GMT  
		Size: 69.6 MB (69559462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c9f036f7d1ffa396ca3e9511b4969c88e3e591452ae52aad63584dee9778a0`  
		Last Modified: Tue, 16 Sep 2025 00:17:15 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45da7434cd322d86c9133e7f4dfe44a44ed7ed912e7b13aedc79512bec0e28cb`  
		Last Modified: Tue, 16 Sep 2025 00:17:16 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.2.1565-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e7b58eb851556652013064097d5079db1d0af4a8a69c6afd9f8afaf43c7fff13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:773e191ecfa9cfb0b77fd625be0d01f63cdfc347738b180c110dbc980f2aa454`

```dockerfile
```

-	Layers:
	-	`sha256:02a891d1af0ea26138a1a6991a731a2a378785ba659fbc3ee2d6ee4c1efb4af9`  
		Last Modified: Tue, 16 Sep 2025 00:42:02 GMT  
		Size: 5.1 MB (5122971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e09f764bce340ff03a10fc9a191c32656d7d4bb4440401b4327099b8e000cf01`  
		Last Modified: Tue, 16 Sep 2025 00:42:03 GMT  
		Size: 16.7 KB (16716 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.2.1565-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:0446cad145ef939741fb9b185a20d33be7bb1c09c18d8cafe22886dd39901407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265543546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c61cca42c22aa7e9cb96f44b18a84a2744ce19d9a4574fc67aa3fcf520f61f16`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
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
	-	`sha256:a438293490bbc2af66661166949a4d86358eeb39f9fadd5b0146666f05b9b9ac`  
		Last Modified: Mon, 08 Sep 2025 21:30:47 GMT  
		Size: 32.1 MB (32068762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64039b52717abc18edb3447e733b9e70731c88eec6dd0becb8335a794fe964a`  
		Last Modified: Tue, 09 Sep 2025 12:34:23 GMT  
		Size: 158.0 MB (157963429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d0356c45eaed2ca3a41586bb4a1ee02956f412880cd4bf803da9fdf6a9ec90`  
		Last Modified: Tue, 09 Sep 2025 12:48:51 GMT  
		Size: 75.5 MB (75510311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a39bc1f0bc58304f0d07559a32f367745fbba359eed6ac115d1fc84af7afb0`  
		Last Modified: Tue, 09 Sep 2025 12:48:36 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9acefab3c3edeab8270b4c3441d8c57a066995baea5bd9adc7098d60146a17`  
		Last Modified: Tue, 09 Sep 2025 12:48:36 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.2.1565-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8a2aca22a9ff416c01acbe92231d464b6a10dc8b95a133fba68c1a921aef898f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be1231838a3bb3fd0fe8891d02c93af17ef8c337d09ac50d4ca18a76d3deadba`

```dockerfile
```

-	Layers:
	-	`sha256:9b17978bd94274153ee78c9dc194f8c95a72e6fc5db3df6c51bdda659f0b7a86`  
		Last Modified: Tue, 09 Sep 2025 15:37:57 GMT  
		Size: 5.1 MB (5122356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68e93f6e4785f5c44746aeca0b56c0f7f627bc54db262e98e1e04eea84e6bcf7`  
		Last Modified: Tue, 09 Sep 2025 15:37:58 GMT  
		Size: 16.6 KB (16635 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.2.1565-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:df4345fe3518fd31aa704abe6da11d093303965276c2fd10759087008a52c396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242396964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12740c0553daeea75ff9a39f4562a35e667b12f58f19675eac228ae94336c80`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
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
	-	`sha256:c235ccf5178d9b6baa6b3965b50fd208e8804504a8dff76fd257b0d061d8dc10`  
		Last Modified: Mon, 08 Sep 2025 21:30:55 GMT  
		Size: 26.9 MB (26884297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edea75e075838ed0aa639f17f3b0b7e49fd14ab0f1d51627956073864e0a9c3`  
		Last Modified: Tue, 09 Sep 2025 05:48:16 GMT  
		Size: 147.0 MB (147026941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51c82b960154169deb7d06e83af13c498875280df42ce494a29168aee95d452`  
		Last Modified: Tue, 09 Sep 2025 05:52:32 GMT  
		Size: 68.5 MB (68484684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f4e35f161b0855f704e04069376037687bb5aa8094218db27a7db86ac7d378`  
		Last Modified: Tue, 09 Sep 2025 06:02:45 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e127eb9da34482c41ddaf943003d7dd7606464b41815a511e4418cd69683e48a`  
		Last Modified: Tue, 09 Sep 2025 06:02:49 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.2.1565-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0d314b9f67198e37459e466e49cfb770b3254bb4cb5d0b702f409dc3712a785a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5125082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7f4067e0bce13c96d5915a21b24763a3c38e0f07e6bc7e928c8624ea88b5290`

```dockerfile
```

-	Layers:
	-	`sha256:78eae0ad5972ddaca51c5561286bfb73cd8e6274c8f1efaab65e871486da0b7c`  
		Last Modified: Tue, 09 Sep 2025 06:38:22 GMT  
		Size: 5.1 MB (5108507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58695126a00d79a74ce51849df44b2f3e9d0fc8c260e0bc151945168d8a4587a`  
		Last Modified: Tue, 09 Sep 2025 06:38:23 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json
