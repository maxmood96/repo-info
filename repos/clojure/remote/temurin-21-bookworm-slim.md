## `clojure:temurin-21-bookworm-slim`

```console
$ docker pull clojure@sha256:fd0ee24c47ca3ba12ad002a6ef3f27457aab4dc9cd052a65fd8d1f945f015e26
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

### `clojure:temurin-21-bookworm-slim` - linux; amd64

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
		Last Modified: Tue, 16 Sep 2025 04:54:53 GMT  
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

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-21-bookworm-slim` - linux; arm64 variant v8

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

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-21-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:3dafa815507d5eb694af313a58c295c67c6b9a8e3d87088bb298b7ba4ae5a274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265543910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c019b505749144f6bf01ff36fb9f806de861cb888991ee45c4a00f9c8d0c23ee`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
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
	-	`sha256:a438293490bbc2af66661166949a4d86358eeb39f9fadd5b0146666f05b9b9ac`  
		Last Modified: Mon, 08 Sep 2025 21:30:47 GMT  
		Size: 32.1 MB (32068762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2959f109b81d6369cb4c4d72db588ee4273715e7579994466fce2c60dd0c1abe`  
		Last Modified: Sat, 13 Sep 2025 03:42:32 GMT  
		Size: 158.0 MB (157963469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ddb6e612e38bfe1d31bc79eaa4a91218af0113aea0401acca73f3db9fa2f72`  
		Last Modified: Tue, 16 Sep 2025 01:19:58 GMT  
		Size: 75.5 MB (75510634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547595f594052e88173cbb223e7930d7cf00577d65805a9799c86a368ce68462`  
		Last Modified: Tue, 16 Sep 2025 01:19:52 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b43e3dd7d0f45d4332c922796190a86f37f6165c0c53ad44cf7d3b1e8c4e3e`  
		Last Modified: Tue, 16 Sep 2025 01:19:52 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3e532b8c4611fd72ce11c533b96e13f515c7605eeddeec6ffc4b4690d24bb333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab25b032e37b74101c02ea60eff662ea00e0880bac4a13af42c97ae036372c1`

```dockerfile
```

-	Layers:
	-	`sha256:90216cd0f5fb6024119b293e24594cb83e80154c1cd6c3b417d5ab2f27e895a7`  
		Last Modified: Tue, 16 Sep 2025 03:40:29 GMT  
		Size: 5.1 MB (5122356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5555c435875480fdec66491a57ca3405d92eaaba0f609c9410bc56c194903695`  
		Last Modified: Tue, 16 Sep 2025 03:40:30 GMT  
		Size: 16.6 KB (16635 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:72d03481b367818b94d2e333510fcc65205e0b9b41625705798b8289bf3970af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242398326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b7c7bce72e89cf3106ec60409ee83cca9d51f24dc9ed92c2c2f8efe4d7706b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
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
	-	`sha256:c235ccf5178d9b6baa6b3965b50fd208e8804504a8dff76fd257b0d061d8dc10`  
		Last Modified: Mon, 08 Sep 2025 21:30:55 GMT  
		Size: 26.9 MB (26884297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209327a5cb75c8c1d8464e1562aa66efe9b66ed99f6f5603c3b5a1ccb9f3d9a3`  
		Last Modified: Fri, 12 Sep 2025 23:55:50 GMT  
		Size: 147.0 MB (147026988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd9c116afa73f36114258aef0c40538832daffcf0bf0ec840e78bcaf20f6fb9`  
		Last Modified: Tue, 16 Sep 2025 00:54:52 GMT  
		Size: 68.5 MB (68486003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094468320bdbf0801a642107bf207d1eeafed3301c0ed7029f1d5e54392068fb`  
		Last Modified: Tue, 16 Sep 2025 00:54:46 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec6687359341b5e28b6919acfa43c5aebd1aa5862e1aef2c65981ba53617b27`  
		Last Modified: Tue, 16 Sep 2025 00:54:47 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:adb4b311fbc09a4b654197ac4078a15beeccec349154e0a6a6ebe93c8c511060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5125082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e20241c3c1e7dfd008f81db99d0c75a7e7576821dc5eafb990c80d6c90d867df`

```dockerfile
```

-	Layers:
	-	`sha256:de1a3d10f321c264ae3ccaa1c1e713a307bb5f59a5a661717fb492a39004af2d`  
		Last Modified: Tue, 16 Sep 2025 03:40:35 GMT  
		Size: 5.1 MB (5108507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fa3f92cde3ea0225c27d691b3ce5eb848baa2f9144b05e917b50f51043bc090`  
		Last Modified: Tue, 16 Sep 2025 03:40:36 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json
