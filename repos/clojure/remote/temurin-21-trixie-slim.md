## `clojure:temurin-21-trixie-slim`

```console
$ docker pull clojure@sha256:da02a8e0958d0c852e3dd6a50d7cd0e82b4d38281710874d6bd0772a5ee2f707
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
$ docker pull clojure@sha256:4af2ff2e5de825350af921d06af09cb432a390fbeaaeae1e8bc68ae5e079c33a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258108300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16af40d6110125623018ae8f73f32be910230abe360f5d1b82a903708fff88d9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:46:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 01:46:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 01:46:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:46:21 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:23:14 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:23:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:23:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:23:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:23:32 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:23:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe9f0ef3f19e27b73c25387a916edb54921830265a7aad870e43390ffa99f76`  
		Last Modified: Wed, 22 Apr 2026 01:47:27 GMT  
		Size: 156.1 MB (156133067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56424479d36d58b87c8df709c51d19e8739a67381ef79cee6e81a8933d068ae0`  
		Last Modified: Wed, 22 Apr 2026 02:23:49 GMT  
		Size: 71.8 MB (71830589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7791b0427a2118e38fec49ec9bf602a40e5141eb188e4f18208d4705ebf311da`  
		Last Modified: Wed, 22 Apr 2026 02:23:47 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e36c55bea7103efc5d01f3684759147015761c79296e6ab5ae1bd8910e57f80`  
		Last Modified: Wed, 22 Apr 2026 02:23:47 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:75150e4eb79ac17c2907b3488a5cbe1b9aafc42e8e03c0aeb5e49ea91235f89d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5282743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec710d5e851fe4fa50d073178465af4a2384d419f32384f44127fac1be687a3b`

```dockerfile
```

-	Layers:
	-	`sha256:d885e8108db92156321f983b3ff5061654f4dd92a2da3fc4eda7578e6dc2bf30`  
		Last Modified: Wed, 22 Apr 2026 02:23:47 GMT  
		Size: 5.3 MB (5266813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:867c1150de788346c4bd25f602582a002a0f68d5865964f01e2ab1851bca9cad`  
		Last Modified: Wed, 22 Apr 2026 02:23:47 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:fb0d7b18f65282c58fb65315641cd938c89641340bdde67430f58daf5661c0c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (269004825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40b215ec59ee19a3d368f3fa712005c97e1baaa2627d151c8d26f24129cc9295`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 08:39:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 08:39:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 08:39:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 08:39:30 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 08:39:30 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 08:43:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 08:43:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 08:43:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 08:43:55 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 08:43:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dfd4a596860411869ba1b27f063b5f93a5f8477634fb7f87b5eea1fe9858af2`  
		Last Modified: Wed, 22 Apr 2026 08:41:02 GMT  
		Size: 158.0 MB (157977486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5c4fc1fe252d87d87f634de9d4959f74889b94261cd41fa96895079b838f03`  
		Last Modified: Wed, 22 Apr 2026 08:44:35 GMT  
		Size: 77.4 MB (77428267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5856612c610965f7f59faf1fedb942be9d213bc3c7950248dd25acb6c3adb4`  
		Last Modified: Wed, 22 Apr 2026 08:44:33 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965742ef595c567d0d01997a3fc68af93ae1b41a22fbfbbab76f10b7649c9e03`  
		Last Modified: Wed, 22 Apr 2026 08:44:33 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7b311006928c2d0c91d904218123e61d1e331e399a3e5b44d70c82099324e60a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4960943bc135bafc50c5d72669b73706c0ca645acef884c9c4555702a5e3c9bd`

```dockerfile
```

-	Layers:
	-	`sha256:37bcb821a7616234773ba0e6ba789b285674359fe03a9531f5604641a2b09088`  
		Last Modified: Wed, 22 Apr 2026 08:44:33 GMT  
		Size: 5.3 MB (5265415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb03b9a2fb0017d8ce9605a794dcd1bb81ce06e24829a9d3da2ebedfdf3603f2`  
		Last Modified: Wed, 22 Apr 2026 08:44:33 GMT  
		Size: 15.9 KB (15860 bytes)  
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
