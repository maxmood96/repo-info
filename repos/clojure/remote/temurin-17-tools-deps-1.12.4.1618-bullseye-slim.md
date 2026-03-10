## `clojure:temurin-17-tools-deps-1.12.4.1618-bullseye-slim`

```console
$ docker pull clojure@sha256:2552de0726ee0a45b8bc0b45d90d2ceba86681933a555262dcc26eadfddbc859
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.4.1618-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:462c56286af2e46477da4fd23b36ad84e147cbf6d3fb22e9f9583b5e7216167a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235071512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af4f556415a11729220665be15db4c027908978c640911a28df463c196cef42`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Mon, 09 Mar 2026 20:35:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:35:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:35:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:35:14 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:35:14 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:35:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:35:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:35:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:35:25 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:35:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:34f0642d22440b5813561cd4375937013bfb556bec8ff3b0e208699b786282a7`  
		Last Modified: Tue, 24 Feb 2026 18:43:06 GMT  
		Size: 30.3 MB (30258379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05099a55c3e3fad9eeecd22d3707625cb31578d9d1d88ffe9ce8de6055b470b6`  
		Last Modified: Mon, 09 Mar 2026 20:35:46 GMT  
		Size: 145.6 MB (145628732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3bc1a23e6840e43cc46ab24c77d93bbe2254ce6cafb1597d56786fc40b01120`  
		Last Modified: Mon, 09 Mar 2026 20:35:45 GMT  
		Size: 59.2 MB (59183356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80a46b97cd5c782b8c8f4bad0bde03299f0392d8f78008eb079000b8fc412fa`  
		Last Modified: Mon, 09 Mar 2026 20:35:42 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce5810c0d5d45dcadb4e3b0a333a57fc22e2741bed8eada923bd740ae3e4dfd`  
		Last Modified: Mon, 09 Mar 2026 20:35:42 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bb85fb7b632761209a3326152a9eb966ae9f0b39ea47fbfe2ae466e55215d007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5337513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e2f2eb5fc800ded91fdb51e576f8de704215f766176fd6288f49ff6630018f`

```dockerfile
```

-	Layers:
	-	`sha256:719cad64bee787c7ce00e38e20343dbf0705e366295b74cb2fd427ddd812c2fb`  
		Last Modified: Mon, 09 Mar 2026 20:35:42 GMT  
		Size: 5.3 MB (5321677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d738018c53f28f3a76f9a790ac285da4e5548db80b707c4ebc4df87bfbf63af6`  
		Last Modified: Mon, 09 Mar 2026 20:35:42 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1c46370b3d99366d74247378f2a3eec04097c4d514a185a9fc7c981a476e3b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232505538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2fff3ba8f1f2d1023127c9c1118a972b19efb3800fd97b40994576405e1cf9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Mon, 09 Mar 2026 20:35:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:35:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:35:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:35:06 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:35:06 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:35:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:35:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:35:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:35:20 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:35:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:018c0693c4a2532e5636d6115333db6d882da8f33f1f40cb3e88dbe62da21aac`  
		Last Modified: Tue, 24 Feb 2026 18:42:36 GMT  
		Size: 28.7 MB (28744470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a782ffd21b3b3887165ba5ad5886ea0277e75b88ed5d73ece9001ba4e0546c`  
		Last Modified: Mon, 09 Mar 2026 20:35:42 GMT  
		Size: 144.4 MB (144436184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7544278630c9177fd3913ad0d28e421e895fcca5beecbde7a7bb27315f93ae`  
		Last Modified: Mon, 09 Mar 2026 20:35:41 GMT  
		Size: 59.3 MB (59323839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3abb395712cbc2b106c6dc0085c5a80481a47d3b09c3e3c95e00dcfcaed5284b`  
		Last Modified: Mon, 09 Mar 2026 20:35:38 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6045a894f2a022848720da4b04fe0509f5daaf21f0d4b0fafc26488c3680483f`  
		Last Modified: Mon, 09 Mar 2026 20:35:38 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8b3a45d4d8fe7e2a0ab90dacf566e20138330646f61512146f49ee610f292353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5343361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c471d5ed194f38e228020c2771101e5fd0b8c5b8081512cb111c73a9d3331f`

```dockerfile
```

-	Layers:
	-	`sha256:dc07779bb2f2bf45d5f009ab6d80aee896b010184caeb7d1f783d60f8e9b214c`  
		Last Modified: Mon, 09 Mar 2026 20:35:39 GMT  
		Size: 5.3 MB (5327409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c254c816aee183f967394f9a72be142af646387cc7bb15b5a037772f216961b`  
		Last Modified: Mon, 09 Mar 2026 20:35:38 GMT  
		Size: 16.0 KB (15952 bytes)  
		MIME: application/vnd.in-toto+json
