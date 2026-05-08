## `clojure:temurin-21-trixie-slim`

```console
$ docker pull clojure@sha256:61eebd194db6407d4f12effafd5c432014ed26c2329942ed8f76be3dd119853a
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

### `clojure:temurin-21-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e6befe1e911977b1637d0fb7ecff49534e5365484767c723a79fadf52cbcd6e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259649458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a50f57ac9fb0d3c9b182dab30f21cf96bd16630deba671b5dc9db1e11c59b9a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:20:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:20:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:20:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:20:13 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:20:13 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:20:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:20:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:20:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:20:31 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:20:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634d32ef46359a2820b42edb940524f5b6e3301f5ca4cc8814968d0c3ebf69c0`  
		Last Modified: Wed, 22 Apr 2026 02:20:56 GMT  
		Size: 157.9 MB (157857104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1239f370a763bb06e37331b4977eb923a16293523b926b4f07852968a76b5ee3`  
		Last Modified: Wed, 22 Apr 2026 02:20:54 GMT  
		Size: 72.0 MB (72011143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2cae559337016ef20c943eb5e79d24b7fa9b93b70051b4fd656de3071b0c8a5`  
		Last Modified: Wed, 22 Apr 2026 02:20:50 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c19bb7fbd5095a7a7f7e6ca78321feabb6f045b7c43a95eee26dfb0cca40d3`  
		Last Modified: Wed, 22 Apr 2026 02:20:50 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8b7b55b3becd2a92655813b3f6525ae93154e05899f62d38ca635cb1d392686b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f8413f6b685301bfab06533f5ead8ab30837a1f536d19537101f9e2404a5be4`

```dockerfile
```

-	Layers:
	-	`sha256:1cb9afdd0251fffa64e1d97fb01e44ced8e33390828f7c1a375f43469ca0c82d`  
		Last Modified: Wed, 22 Apr 2026 02:20:50 GMT  
		Size: 5.3 MB (5261044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3492b97d2ca00d2f3a4b4f36725ca85a76da92ceef859a75333e189b6ad6f691`  
		Last Modified: Wed, 22 Apr 2026 02:20:50 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:be3437bed3666d9199bf6578819379faa26905d7fbd2af3063f9754864abdc0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258437255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7572a0ad8b2362ccd9bb8a5ec166fcbabad69e32c4c9e83610ed7adf2df4fbda`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:26:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:26:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:26:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:26:53 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:26:53 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:27:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:27:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:27:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:27:10 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:27:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce602dbc3abdffe79bd19f3807aecc10ff5f624517234e7d26eca130f6e352b0`  
		Last Modified: Fri, 08 May 2026 00:27:44 GMT  
		Size: 156.5 MB (156461191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e576b3f16ddb0564aaa4b4cddb519aebb2b02790e6c546cee63f0f3ab93e4ea7`  
		Last Modified: Fri, 08 May 2026 00:27:34 GMT  
		Size: 71.8 MB (71831416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d22cee384a59bb5d23c1c78c8bde5e04fa301e781506fe785c383683ced2b90`  
		Last Modified: Fri, 08 May 2026 00:27:31 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a967dfd3f368e0b9f2747f4e49ea0783269c3c1903843a72a96dad15abd2c85`  
		Last Modified: Fri, 08 May 2026 00:27:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4502e8e306e26cd7d62e69440473320b7ac383999ab31285cdb6ae521be45298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5283523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:953f0b90f0f55bde9751b95ee5610bcfaa42e459e5cfbaad47132a18d29126a7`

```dockerfile
```

-	Layers:
	-	`sha256:83b60f3470ab3e065b340be3b6de5be730d33b91761e366e3ff367eca051dd37`  
		Last Modified: Fri, 08 May 2026 00:27:31 GMT  
		Size: 5.3 MB (5267440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2a8f4dda3a5d498164adacf775d3f353faf72b380a8686cf83288e67b197436`  
		Last Modified: Fri, 08 May 2026 00:27:31 GMT  
		Size: 16.1 KB (16083 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:ad569ca1a4a8164b18f94c58792ba65056f5d5cd3133a0e94db1a073a1aa8cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269370757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf5236e5f834e916151bed93c749b68d5dabb9c8c6bd7190a10be8a24de337ff`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 01:38:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 01:38:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 01:38:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 01:38:54 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 01:38:54 GMT
WORKDIR /tmp
# Fri, 08 May 2026 01:43:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 01:43:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 01:43:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 01:43:17 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 01:43:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679bdccfa02f117dfdaab6da4f7459875679357ae8fcbf2cafce50f771adcbf9`  
		Last Modified: Fri, 08 May 2026 01:40:03 GMT  
		Size: 158.3 MB (158343276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72a100c5b508f4ab7a4d7c55049ea73eba39e81620ab5e1c1c64825fb2b78f0`  
		Last Modified: Fri, 08 May 2026 01:43:50 GMT  
		Size: 77.4 MB (77428407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8cad1daeb3f63f143955f66db15d904595e502c6a98eb4b66962da785e795ba`  
		Last Modified: Fri, 08 May 2026 01:43:48 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0110f3269e641a29d815ab6522158ba27837b3152fe54c068ff06cb11a4c8b8f`  
		Last Modified: Fri, 08 May 2026 01:43:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:667b614e3e69dba2ecd973eeab0f93a36b420eb96c08d6f3a3fe9a062adde695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5282056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e7b8a463eb6583d6648784a579967cab4a90d49ea7ed5b3dcb3ebfe457008a`

```dockerfile
```

-	Layers:
	-	`sha256:2334dba447e7b3106f18afe6ff3bebb907e662f3ca48ad9ebcc73a701b749440`  
		Last Modified: Fri, 08 May 2026 01:43:48 GMT  
		Size: 5.3 MB (5266042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ded831f7a9014f3e75a3dc0c9f51bdc4d56472de24de937e2633fade14c4a82`  
		Last Modified: Fri, 08 May 2026 01:43:48 GMT  
		Size: 16.0 KB (16014 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:e6d432b91d36cd2b88b5455fdafcac9c13289bcd95f8b9356be3cff46d87f204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256399009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7fe55935cdf2e86fbad57699882820ef392e62a4126707262cf382ea01d70f1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Fri, 24 Apr 2026 18:16:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 24 Apr 2026 18:16:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 24 Apr 2026 18:16:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Apr 2026 18:16:48 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 24 Apr 2026 18:16:49 GMT
WORKDIR /tmp
# Fri, 24 Apr 2026 18:33:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 24 Apr 2026 18:33:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 24 Apr 2026 18:33:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 24 Apr 2026 18:33:45 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 24 Apr 2026 18:33:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad178a1c7448a34e9758387fe35c9fb467bae057770eff7c342592f312ccf326`  
		Last Modified: Fri, 24 Apr 2026 18:22:57 GMT  
		Size: 157.2 MB (157216929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4485bc2d2d4e9d9b14618767c526aaad37b1c9472f8b95e2e7b23960e4058890`  
		Last Modified: Fri, 24 Apr 2026 18:37:35 GMT  
		Size: 70.9 MB (70900843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae62c404a6f55650f01f12b354e9822d5b9493c881275d1223b63eb371682c18`  
		Last Modified: Fri, 24 Apr 2026 18:37:23 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8432fbb1b29e2115e227edab6b25238e1ce682fcfe4fee77ca3adce673515de`  
		Last Modified: Fri, 24 Apr 2026 18:37:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:262c1c3d07d5e8026102a41c1d4ae8a94db44996d7c0bc8d1df78774b8f384d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5266368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdbf695ddc49d9cd3757d3374b562cfe76b8b2ab6a9abedc7e116eb1c8b6ac59`

```dockerfile
```

-	Layers:
	-	`sha256:7375f39b227c4d8068a20126d3c4d39b4c8be91acc66e87dd9be88778a52485d`  
		Last Modified: Fri, 24 Apr 2026 18:37:25 GMT  
		Size: 5.3 MB (5250508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:531bf999926f50cf962a1cead605783cc6fa62497d88966af945f38372572747`  
		Last Modified: Fri, 24 Apr 2026 18:37:23 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:8c2c4a3b5e47c07e9403a6a71aba661470f0ef67df89f0af34a3c0ecfef4d2da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.9 MB (249933538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ee563da328c4555790bb930718e01d7d66e6ff66cc6a0f08ed80bed7dba986`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 04:03:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 04:03:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 04:03:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 04:03:16 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 04:03:16 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 04:04:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 04:04:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 04:04:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 04:04:30 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 04:04:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc13e0424f9cc62cbd79bd2740a0337d43290a60f702b3f4c6b3ca57b188dac`  
		Last Modified: Wed, 22 Apr 2026 04:03:57 GMT  
		Size: 147.1 MB (147105211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9878362713ffd3ee177577e0cff1f477287dbdd5b05c252ddf9a6040447891aa`  
		Last Modified: Wed, 22 Apr 2026 04:04:55 GMT  
		Size: 73.0 MB (72986987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0577277d9b440b3396f80beaa8875b0830f6f41012a1cb5e0a029d82a5bf6e0`  
		Last Modified: Wed, 22 Apr 2026 04:04:53 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0acd54b9726b9544b115b971c169a6eddb0e59f8d061ea60b11681774d568e7`  
		Last Modified: Wed, 22 Apr 2026 04:04:54 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:210d7a46df8363d036b601d730290684b17b18554621d1988228ace197407383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b02545415b6703fc0b44b6aa6a925318ca1faf7c16fd3ce4c5a73abe04b05656`

```dockerfile
```

-	Layers:
	-	`sha256:2af145bece0bfd03f71256c777df63d9a5ae6b9cae6f8a0f4e113b3a4c51d0fe`  
		Last Modified: Wed, 22 Apr 2026 04:04:54 GMT  
		Size: 5.3 MB (5256968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e11580c497de683953e5d4e23efb432f8d54d7258d262f60f56d036edfb9021`  
		Last Modified: Wed, 22 Apr 2026 04:04:53 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
