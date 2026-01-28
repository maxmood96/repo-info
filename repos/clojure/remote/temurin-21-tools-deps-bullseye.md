## `clojure:temurin-21-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:56bc4e4ddd62feab486edd4fcfa161384d4bdd7fd80c83b3c68e6dbfe4ea8893
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e399c0d244d7dd65baf28e14af114f951fcd9e77e285ef7c048d78f482c442b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 MB (281125159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ac4c9ad9d9616b7e461070fc14ad416f7dbe35e68a88ee2fd108117196993a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Wed, 28 Jan 2026 18:05:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:05:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:05:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:05:44 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:05:44 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:05:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:05:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:05:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:05:57 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:05:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fccfc62cb15165379a658b98df1680b95e3908f69adc8e7176a095a7b4cf2106`  
		Last Modified: Tue, 13 Jan 2026 00:41:25 GMT  
		Size: 53.8 MB (53756446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa99e048ed03afbc12e22bcf51b33a8ee28833a9e3aae01c462f3f22182cdd6`  
		Last Modified: Wed, 28 Jan 2026 18:06:20 GMT  
		Size: 157.8 MB (157826002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3c7b916fbb06060b8b3998a77c6ec28844c45c0d5c3159807e6c7bc73b31ef`  
		Last Modified: Wed, 28 Jan 2026 18:06:19 GMT  
		Size: 69.5 MB (69541666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64cf9d047936762706c064d3eb86675786914e79d739ddc2c79c3a3116657a13`  
		Last Modified: Wed, 28 Jan 2026 18:06:16 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfa3f32cf4e79e73e1c2aa9eb0e294d07336c96bfc78f777e75c75c57da77f0`  
		Last Modified: Wed, 28 Jan 2026 18:06:16 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c3c503ceb2e719c1f82616e2a642afe41c6a04b34832f763ba3d8e295ed29b79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7415348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daaa05f54e69e1c51ef30e7089ee0b830beef498d446b8eba94861ab8a2d5d11`

```dockerfile
```

-	Layers:
	-	`sha256:2c35ac7b9a4bf9ed14ab00aa9de09a14ca943caa479740d1d584d5068d6cc3ae`  
		Last Modified: Wed, 28 Jan 2026 18:06:16 GMT  
		Size: 7.4 MB (7399570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7081f7cd5ccdf115a2f5b5de32954a95e4935c805a1e5eb4bf3c36e96bf8a4e3`  
		Last Modified: Wed, 28 Jan 2026 18:06:16 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e876466258549be274111eb9a2a288aa7508ef7a1337096f9f8ee2b662242f4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278059686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2edd6f48bac385887823d42333cb82612ba513fcf84b1e0b1e6fce878ee5aeca`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Wed, 28 Jan 2026 18:05:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:05:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:05:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:05:18 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:05:18 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:05:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:05:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:05:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:05:32 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:05:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:31 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160765f1970519a0e62c40d8e0a715dcb590fa304eaf952c7aa96f092877b5b2`  
		Last Modified: Wed, 28 Jan 2026 18:05:56 GMT  
		Size: 156.1 MB (156107578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512e3b9aa483636c530f129ff18967782186c3f600ae2568c01182bb62edb194`  
		Last Modified: Wed, 28 Jan 2026 18:05:56 GMT  
		Size: 69.7 MB (69693298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0159d8a6e6de52915456a45343e8d9bd2ea5cfeb06daa4a389884fe1e05f9fba`  
		Last Modified: Wed, 28 Jan 2026 18:05:52 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583974c7868ae87967cebc96d648ad372ac0a3c8fdbb04a1f534e7160ca98850`  
		Last Modified: Wed, 28 Jan 2026 18:05:52 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:818eed1fca7184047d1c8c780eb7367b36e1c35226232095b295befe603b8244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7420565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8598df0d9c46d0dc253965400064550c6ab4b5556081f133fc207ce9179d064c`

```dockerfile
```

-	Layers:
	-	`sha256:ab2b7d3b127bfb2ac3ffe40e1a5eff725320745ac0a93499e28df68aebc68c8e`  
		Last Modified: Wed, 28 Jan 2026 18:05:53 GMT  
		Size: 7.4 MB (7404669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:517d011c75c11277e73202fc098d15757c2f6250e79ae28a280e84d6de88a8bc`  
		Last Modified: Wed, 28 Jan 2026 18:05:53 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json
