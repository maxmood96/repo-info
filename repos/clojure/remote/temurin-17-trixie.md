## `clojure:temurin-17-trixie`

```console
$ docker pull clojure@sha256:a844b86ae12979dcbd2551ecabec547299a57755fbbc5264405457831d7b1a24
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:f4578d99933e42009fdb63d1cd5c30be9a77a9757f12cd44c00429eb2d1de0b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280495157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:561369e9af9b4e2dcf2e907957dcfecd5e9e7e8daaa2bb6f7e16e0a2de5197d9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:15:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:15:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:15:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:15:11 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:15:11 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:15:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:15:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:15:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:15:28 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:15:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4984dc819b89987a22cd1799ae1f1e25122e44a92526a9199ee7a47e67e30ea`  
		Last Modified: Tue, 07 Apr 2026 03:15:51 GMT  
		Size: 145.6 MB (145628687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238088cf7af740c7b3166bea1b0d1c782b6ade3f5c3bc1959edfd1869127724c`  
		Last Modified: Tue, 07 Apr 2026 03:15:49 GMT  
		Size: 85.6 MB (85567594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678b6d47731322d0a056ab3e872779aa3af6af05ffcc06c75432643b4af6cee5`  
		Last Modified: Tue, 07 Apr 2026 03:15:46 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683441926719e93b88e18665ffa577ba95b3fb877fed89383a94c7ecb392440d`  
		Last Modified: Tue, 07 Apr 2026 03:15:46 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6c3ef270d0a1ffdcc9c37cbaee961597df8f9554cde24a786f8876d87ea2e373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7486421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d657798e593a2db82cb8273158ce9dbf8a223f8cd6f1cca543c35ae585fa5f4c`

```dockerfile
```

-	Layers:
	-	`sha256:84b70a2e636998b5c84b70286ef8f00ec2f7605f8b16e952837b65dcbc5f902a`  
		Last Modified: Tue, 07 Apr 2026 03:15:47 GMT  
		Size: 7.5 MB (7470667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e08cec223062a36c0b5bd63f50638084d44228d0710ca0792bb98ccffaf81e93`  
		Last Modified: Tue, 07 Apr 2026 03:15:46 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4438a51405bc0694cd9c87f697491c69d912649a181e6ea8ccb3bca5b13ecd2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 MB (279485688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af297c748470ea797a51a402819879bfe9e32eba4d76fdb1d0c6499cbae390bc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:25:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:25:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:25:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:25:54 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:25:54 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:26:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:26:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:26:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:26:12 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:26:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99780b28a51709ddd21e604dcfc6034f1e9fb5694e088f78ff893724e562bf0b`  
		Last Modified: Tue, 07 Apr 2026 03:26:42 GMT  
		Size: 144.4 MB (144436226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214c63e47f8e1ce9bc7ec9fab88686bf21b16247895286ed510b1cbf2dd1cc8f`  
		Last Modified: Tue, 07 Apr 2026 03:26:40 GMT  
		Size: 85.4 MB (85383166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afba83f5648d7f8c2715fd60a6855c75477b2206891f7e155d6d00850d566ecb`  
		Last Modified: Tue, 07 Apr 2026 03:26:35 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06e0bb3f4998ec593e1d60a8ab85e1df4b4aeb27029a000a79076ee85eaaacf`  
		Last Modified: Tue, 07 Apr 2026 03:26:35 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6b1cad40fed13fd18605408464670582cf46e7fba9d199d1222406f6cfedda2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7205294098bc9311f588139e4a81484324911676d7d44f215e325cd2d0e79e82`

```dockerfile
```

-	Layers:
	-	`sha256:20b7505163d75e31e73ba4722898fe414d7cf0ffda7d0a3648d774e208aa1bde`  
		Last Modified: Tue, 07 Apr 2026 03:26:36 GMT  
		Size: 7.5 MB (7477697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:792a8db0d4156521ff88bf134e9b1afb3fdc302cfee4a395276ad871e4117ae2`  
		Last Modified: Tue, 07 Apr 2026 03:26:35 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:ea85fe358485cdf7cc3aa12379a656105a390030049bb22788583654b274dffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.5 MB (289544935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c909ab2b75ae9472308f5002d4194e8b7359342e6740a7805a7f21645e66bf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 18:27:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:27:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:27:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:27:35 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 18:27:35 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:33:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 18:33:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 18:33:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 18:33:38 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 18:33:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:616ed6c40b4f1136ebcda954e46e021bcee567aad248468321da4f4065f4a14d`  
		Last Modified: Mon, 16 Mar 2026 21:55:32 GMT  
		Size: 53.1 MB (53118350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822c66d457280a71230ad4487fd70323ef90d3d8e95b8850297f2bd84ecbef19`  
		Last Modified: Tue, 17 Mar 2026 18:29:06 GMT  
		Size: 145.4 MB (145438236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5cc19bef13ae96c0db875f9ffb4a98f1a658a98ceb3f505616c3924652dccec`  
		Last Modified: Tue, 17 Mar 2026 18:34:16 GMT  
		Size: 91.0 MB (90987307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5fa96209f5785aee388bd7f46c3e7c35f19f697cbd57036f3cb442ea75ec434`  
		Last Modified: Tue, 17 Mar 2026 18:34:14 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981e429fbe00995188a27439e4540d4fdba8fbafd17798be12f36146b7e9d06c`  
		Last Modified: Tue, 17 Mar 2026 18:34:13 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c7f16750d009579c6117a3b8b0fd4b1b15c44b1131a7b702aa0942b37426e5c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7490890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5de498a0417d403aed543dcfab76f5e6e5c3f01d0cd051e982f9f403a456ce3`

```dockerfile
```

-	Layers:
	-	`sha256:18b363d2f04bf96bdc30b04933ea5ddafbbd0d6291ea1c75f344ddbff0bf6776`  
		Last Modified: Tue, 17 Mar 2026 18:34:14 GMT  
		Size: 7.5 MB (7475088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89322619e4e6586a48c7f7d0880d50eb3a5c5faf74910535fe4843c314f9cb06`  
		Last Modified: Tue, 17 Mar 2026 18:34:14 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:b33e1ee4a6c9da0dc71ac96a98f92c5b8d8ee9b405fc175462c866b6717b50d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.9 MB (274915328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b63e01ee344b7ed34b37109c8511696f150370dedfbce474d752f6f70b3d81d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1773619200'
# Sun, 22 Mar 2026 18:22:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Mar 2026 18:22:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sun, 22 Mar 2026 18:22:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Mar 2026 18:22:07 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sun, 22 Mar 2026 18:22:07 GMT
WORKDIR /tmp
# Sun, 22 Mar 2026 18:31:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sun, 22 Mar 2026 18:31:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sun, 22 Mar 2026 18:31:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sun, 22 Mar 2026 18:31:27 GMT
ENTRYPOINT ["entrypoint"]
# Sun, 22 Mar 2026 18:31:27 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:90acba8ac92ad141ae919a99e64549b2f417e5b2ec79f1a99dbc8efba0fea96b`  
		Last Modified: Mon, 16 Mar 2026 22:09:11 GMT  
		Size: 47.8 MB (47792328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6add0609c3b541666acbd64d7040bade8e52829cb99e1fb5d81f0474186bee1e`  
		Last Modified: Sun, 22 Mar 2026 18:28:10 GMT  
		Size: 142.7 MB (142662936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9c93f4e8bb065bcffd80f6b184be8912a632fc411d8b8cbb05f94a47333d7b`  
		Last Modified: Sun, 22 Mar 2026 18:35:53 GMT  
		Size: 84.5 MB (84459022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69f072ba7cfc17ae4e5ef896fae0daeb2e5c183e4729f70a9c962764ce05ce1`  
		Last Modified: Sun, 22 Mar 2026 18:35:40 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d6e5d38dc147f687452d263c92d9e317f90c54db964d8704df3724ffd8952c`  
		Last Modified: Sun, 22 Mar 2026 18:35:40 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d9e3ceb7215b526ab15595dc7fba34f7056072cca3a19c2a9d717e74c742bc02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7472465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2309d99270742ea389ea4c82c30b37a20e29dd79d6d31ec8a21fccea7a6543`

```dockerfile
```

-	Layers:
	-	`sha256:f068f99564984a0aca677370c89e804dca1d46035e8347d7d21e0a3bd92a208f`  
		Last Modified: Sun, 22 Mar 2026 18:35:42 GMT  
		Size: 7.5 MB (7456663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f517eb3dccc51a3ec0196e28bc8f499d8860e34ac8f54594d9dcb59861857c9`  
		Last Modified: Sun, 22 Mar 2026 18:35:39 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:f163303f7d2f71753b0aea2a1392138a1cc888e3653c0be4ea97d740cde0efd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.5 MB (271537285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:635e2c39cffd55a05f4471a066e82482357b824e2bc00057720f72f05b2b0638`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 05:42:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:42:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:42:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:42:18 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 05:42:18 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:43:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 05:43:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 05:43:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 05:43:37 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 05:43:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:99ccdb9e0b0ce79a36cbcc433fd972b049c1e4e84d217954de0e89224b1fb094`  
		Last Modified: Tue, 07 Apr 2026 00:13:49 GMT  
		Size: 49.4 MB (49365104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5be30173782ac514fe3cc2acff6571642739faff5843cc6d1d0067cb9203c3`  
		Last Modified: Tue, 07 Apr 2026 05:42:59 GMT  
		Size: 135.6 MB (135626852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fca09ee2833a47ae6fea387cb5d65815016ac3269d5f2fa97f9dc7d2d0bd43f`  
		Last Modified: Tue, 07 Apr 2026 05:44:09 GMT  
		Size: 86.5 MB (86544285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ed6606350984a889612232a18bfc823aa6134efb85a1ceb80df3f7bcbd1534`  
		Last Modified: Tue, 07 Apr 2026 05:44:03 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd9bf6b70b67aa4787f7dc8b2b3d7c36ff446c056a9ac76b6909477a7e7f661`  
		Last Modified: Tue, 07 Apr 2026 05:44:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7a4cfa83db351ef6d8a566ef9c4867761430b819c5325b30130f073a0738deda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6ecad5cf61e4689e00fed9be3ad798c964c658cc1ac101e75dbb8ebe30592b6`

```dockerfile
```

-	Layers:
	-	`sha256:63afe970de3a078b35ecbb5fde1048f3fdcd850e9b443ffc412424a086e04c1a`  
		Last Modified: Tue, 07 Apr 2026 05:44:03 GMT  
		Size: 7.5 MB (7466589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0577f44187c96b37b10dddb17cec65a05d6d233be9df703d38735b43dc357dca`  
		Last Modified: Tue, 07 Apr 2026 05:44:03 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json
