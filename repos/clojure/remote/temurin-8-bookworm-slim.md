## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:469c09e44ddc13d7f4462d1fd4e92d48d825682a7fe097348affaafb4ac227b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:aebe3942a7027ba3db02d8638b5b7c8f1d67296d285895d0bff22c1461fbc349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153105988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8703fc4e53043c6e1cb21cc3a8af08a940774a38f74dc59bf4eb1c0bebcb28af`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:15:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:15:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:15:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:15:14 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:15:15 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:16:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:16:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:16:01 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1eff77e6a51c17b6e3a08fcd3a36c13d776376f3c2df207e788ca742c27b41`  
		Last Modified: Wed, 22 Apr 2026 02:15:42 GMT  
		Size: 55.2 MB (55170060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2559fec94ac7e6b1709e2ff6810d08cbe026a33551fecfe9600f5cd213fff9`  
		Last Modified: Wed, 22 Apr 2026 02:16:16 GMT  
		Size: 69.7 MB (69699031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0326e34e4cd2162cce4567026c89e4c669fd12dbebf41279626e826a4eb3387f`  
		Last Modified: Wed, 22 Apr 2026 02:16:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6f624fa75244f5e50f65f9202523b08f660008354ddbeedaf12cbb014e668b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5250602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc8cfbc2491f40c4cb80f1682daf6941f41f8d133073b500778d7bc3d72ad36`

```dockerfile
```

-	Layers:
	-	`sha256:6d86276228bd3c1fa6888e169195fe50d014872904e0dce11d3726d284e4cb8b`  
		Last Modified: Wed, 22 Apr 2026 02:16:14 GMT  
		Size: 5.2 MB (5237154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0feadac2efd90d4f42670f517dd7e96022ce36708a60f4d18641aefbb7e6875`  
		Last Modified: Wed, 22 Apr 2026 02:16:14 GMT  
		Size: 13.4 KB (13448 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:555d207275b59a765138f9daf74493bcdfa48dae5a85e7a48ecb44ddea5d498b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152060940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab1b04c93e92790aa2ae9924567f818c5d16e8104f8da9c45bac9b2d4e7e2e9`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:19:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:19:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:19:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:19:35 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:19:35 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:19:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:19:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:19:49 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ac91cdd85102d1953a604e0d67f5d00c6ec829babaf3b2c1e0ec8e06f676be`  
		Last Modified: Wed, 22 Apr 2026 02:20:07 GMT  
		Size: 54.3 MB (54251620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59200be205125faa38d9e82731b59342b0bab6d2ffdcd158165d2fa79884a211`  
		Last Modified: Wed, 22 Apr 2026 02:20:07 GMT  
		Size: 69.7 MB (69692561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57898dfb882d85f9d19ed5b58a476200d7b0898a0f70a65411f68eddbe93cde`  
		Last Modified: Wed, 22 Apr 2026 02:20:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3dfaefee72ba905616a8c604ba400cc520e06e3bc923eda97d4ee4a0ca0a2f11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5257981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c514c850caec949a1be2ccd0b53f35623b586473eab46db5a75bd61e8906ebe4`

```dockerfile
```

-	Layers:
	-	`sha256:400e95bc415a1c4880997f717de9cd0314fdd47d0908df1077375e7a12bb9d9a`  
		Last Modified: Wed, 22 Apr 2026 02:20:04 GMT  
		Size: 5.2 MB (5243615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:020e46689745d4bd771ecb5c8e31acc52bf480c3650a3d14969dd987dd3705f5`  
		Last Modified: Wed, 22 Apr 2026 02:20:04 GMT  
		Size: 14.4 KB (14366 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:9c890a7c5256c17ee0de5bed0f7bd6f3d36fb403eadc356b2a9030dcb2043d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160259482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fa3c3ef7f08ed0805a90e2115bddf93fd90cbd0180d1c7a516f1972fc49a1cf`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 08:14:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 08:14:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 08:14:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 08:14:52 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 08:14:52 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 08:18:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 08:18:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 08:18:10 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0bcb46f6315f7a2c8ddde875fca21de96c94e451046e6692f77a99aca489f3be`  
		Last Modified: Wed, 22 Apr 2026 00:15:02 GMT  
		Size: 32.1 MB (32078402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b356cbf5e863ec8292624dee180661bf4ceafce1ae834eda77f2b34cc77d309`  
		Last Modified: Wed, 22 Apr 2026 08:16:00 GMT  
		Size: 52.7 MB (52650390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed17d55a60a3f914c68c6debbad553ad12a4276e9c2ea651a6cce28f3d0b2e5`  
		Last Modified: Wed, 22 Apr 2026 08:18:50 GMT  
		Size: 75.5 MB (75530052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8f01ff2a62a97102a8f2390cdc46e3d286b61a08de1158ad526969a9a24544`  
		Last Modified: Wed, 22 Apr 2026 08:18:48 GMT  
		Size: 606.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:29780c4d66d250eb0e2b9a11e21bfb859cffe3d7f959969e7b701b6e78989705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5257202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8068ba0890e67b7e6c98b4d5fef490fdf5540eccf7e71ba3f00b737b65f95cd`

```dockerfile
```

-	Layers:
	-	`sha256:e3012ff46cd00613b434999d588e4059868f7134aee3fb1d37f7ead13c6320b3`  
		Last Modified: Wed, 22 Apr 2026 08:18:48 GMT  
		Size: 5.2 MB (5242907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfe46ba70edbfa04f0fb06d097df2061a74fad1136e5b5888aef0df979107b19`  
		Last Modified: Wed, 22 Apr 2026 08:18:47 GMT  
		Size: 14.3 KB (14295 bytes)  
		MIME: application/vnd.in-toto+json
