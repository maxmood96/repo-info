## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:93e7da0487c3db74a116185009afee7ca9f5431d0b13bd2f55f7fd0dead69639
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

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:714d53a336e3934ec53f3bb8cae49680b89801ccd89bf2c7dba93fddc1090881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 MB (242602865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7943246ddc84fa3dab1eda4c8f05d9299788aabe26a9c394c617315b7fa5650c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d85ab7966628e5c1fa1b103fa6dfe3d5911dfdbdce5f20292e908e032bcfba`  
		Last Modified: Fri, 03 Oct 2025 08:25:41 GMT  
		Size: 144.7 MB (144693635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fab3d0953fe9d9a355721744edb521accd0845406cceb06b0f3da054a87135`  
		Last Modified: Thu, 02 Oct 2025 08:59:08 GMT  
		Size: 69.7 MB (69679854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcff6f1798102d726dc3b3f45ea54d98637085f93a430060582c2b01571e3545`  
		Last Modified: Thu, 02 Oct 2025 08:59:02 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b419c6227cbae3804915a3cf44d9a77f06f01852e1a5a57721a71735fab8a92`  
		Last Modified: Thu, 02 Oct 2025 08:59:02 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9b14a6cb75dc351509f88eb4e801d26b1b833822bf01c45a04270df1a186a59a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5129267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b550e521898509be5b85ad5a9676442e0396977ff81e294cb73bf8bb3baecb7`

```dockerfile
```

-	Layers:
	-	`sha256:f6da703ecf9b1868f4ba9e0d86961e5428c5cb8dd4d54bb9d31eed31c64172ef`  
		Last Modified: Thu, 02 Oct 2025 12:38:10 GMT  
		Size: 5.1 MB (5113388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:023f9a0b4603b89f91fce7718c7dd5590d7a9f35471fc174f936fba9e1c808dd`  
		Last Modified: Thu, 02 Oct 2025 12:38:11 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c2910b3a206cd00039a25e548713b10d29d06b8e1a737b580e2a00f28a6e4f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241205546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26d79db8e7addbf2f3011e32ed57ef2f7ef71bbdf0da8de1d9dd9d31a21f733`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8322a0329386eac072606736f31318a874360d536d5a7045d246c0dd874b1f`  
		Last Modified: Thu, 02 Oct 2025 07:37:20 GMT  
		Size: 143.5 MB (143542106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b74ac31e93f28716a763fb9f3844f68bfadadb0b2eeee1b4518b20236f3e90`  
		Last Modified: Thu, 02 Oct 2025 02:44:05 GMT  
		Size: 69.6 MB (69560256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a12e79353bfb860baac202a59f6965cd09dcd0db18720640ec5acaa2d3a0ddc`  
		Last Modified: Thu, 02 Oct 2025 02:44:01 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07423bb38589c50dd32b364107da27001c7278742faba2c22841c33bbf44711`  
		Last Modified: Thu, 02 Oct 2025 02:44:01 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f1c1669a59854579e4c3f9444f829ea1a9e8f6230f27c5eb0df093c3b6140ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5134345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72b5cc447110174c0b0e584b474dd40d843a378d40a899a9b915f9254f5a0e5b`

```dockerfile
```

-	Layers:
	-	`sha256:864c47946cd22edc51a3e5cea2e19e074e02127bee7edb1579cdf11bd9d99b6e`  
		Last Modified: Thu, 02 Oct 2025 06:39:03 GMT  
		Size: 5.1 MB (5119149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96f221e8b4f61cb13018981b29ff3bd8f1a66b86001d2c820fbf708dde25e359`  
		Last Modified: Thu, 02 Oct 2025 06:39:03 GMT  
		Size: 15.2 KB (15196 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:dfffb6b34dfed590880e9c0090ea22b703bda42e0e5ddf93f1afca77d9e82e40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 MB (251955388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b14f7f184e6f1de7182d0c2b472b2e2bd9330e8da07be40285f5b6c5f1b4182`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2dae4fd387571f8090d4bc2fed08c7939fa2ac7aed0e2814aea4306333899e47`  
		Last Modified: Mon, 29 Sep 2025 23:34:09 GMT  
		Size: 32.1 MB (32068697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e64cb9b1fb420f1a208861127191d75bd311de4a17fd7799a873fa3425883a`  
		Last Modified: Thu, 02 Oct 2025 08:45:15 GMT  
		Size: 144.4 MB (144372655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5813ac970290a8d67c8e8e9b79ace5883fb922fc46f3c0d911fbdae4d4550c`  
		Last Modified: Thu, 02 Oct 2025 08:57:28 GMT  
		Size: 75.5 MB (75512992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e272b2dbee35444f8b1e3d392eb7475ce7e733ae74c4ad89b3fa3133d7440d`  
		Last Modified: Thu, 02 Oct 2025 08:57:26 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd588da2eaa8238d0619bebb3e955b0f81010a053fb94474d8037f195ff2c649`  
		Last Modified: Thu, 02 Oct 2025 08:57:25 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ce5444e66c635ee3ec66454149c6921c5b966f84b2b926765db95c55cfd90e9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5134472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d2fe1abc1e7b93fb3a03dc85b565b28fff5c9bd7e1c9e917a28f0cbdb72c558`

```dockerfile
```

-	Layers:
	-	`sha256:505450783934cf7e51b10918a0601185dc32cf4791579247c06c5a9b985ee0cc`  
		Last Modified: Thu, 02 Oct 2025 09:37:12 GMT  
		Size: 5.1 MB (5118546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f50ae655f7108eb0d4ab792e7c04b2de5226cdcc3a81bd29153d9218ba81e2e`  
		Last Modified: Thu, 02 Oct 2025 09:37:13 GMT  
		Size: 15.9 KB (15926 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:41be7917501eaa943badf305685bee0cde00c583e49b8072c5283335667d85c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.1 MB (230100082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1417b447b96c458c42089e741b8e452472f8c46cc0a2a00ec0bf365f00500b32`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ee23af7e2c95e7ad71a0f6edf7e138d45ffffb442811e2b9572806a68ee1338e`  
		Last Modified: Mon, 29 Sep 2025 23:34:05 GMT  
		Size: 26.9 MB (26884320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673d91934657daac3b3a5d6dba56e4c4c6906a729705bec1f1b1d392ec897526`  
		Last Modified: Thu, 02 Oct 2025 07:38:56 GMT  
		Size: 134.7 MB (134724220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616392afbe491a830cd8fae23688e0567a214f3bbe3dd6f772efc79255edd145`  
		Last Modified: Thu, 02 Oct 2025 04:37:02 GMT  
		Size: 68.5 MB (68490503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b4827dd5cdda035dd0b9eea70c02c06ae0c30299e397803c2fb259b69cb39a`  
		Last Modified: Thu, 02 Oct 2025 04:36:55 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e210373ad2cd6eb56490b351694a9285d8305757b5e4513877fbec4d3d84fe`  
		Last Modified: Thu, 02 Oct 2025 04:36:55 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fcc68ccd677cb1cb94dbe5bb0b6356c363773f0a648bd97c5a94887a37c4041a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5120587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb6b3709eef8687dc6190ea582c00396d839c88c57f4909c5e8ced1b813520f`

```dockerfile
```

-	Layers:
	-	`sha256:f588288bd44771c11c7373281ff86805ffcfe49a41bfba855d69ee2150cea4c3`  
		Last Modified: Thu, 02 Oct 2025 06:39:11 GMT  
		Size: 5.1 MB (5104709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6d66658eafe7cc27eeebc3a6ea418d0099cd39f830bae3ff869a48c2c8668ee`  
		Last Modified: Thu, 02 Oct 2025 06:39:12 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json
