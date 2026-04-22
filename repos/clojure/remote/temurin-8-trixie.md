## `clojure:temurin-8-trixie`

```console
$ docker pull clojure@sha256:76dc441ee4fba8ac6d356771861049bc3cdda7ee4a76ea695e2e2ad90da7ea0e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:710a142b1e059febac4037ee762fefc74acb0d141457bda3c2bd148cccfe3693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190043274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9268de6537be6a2f770fd0af35a0d499f412cbb1c782d05ffcacc82766031128`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:16:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:16:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:16:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:16:33 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:16:33 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:16:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:16:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:16:51 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b913c90c36f25267ccabd0656a54674795ddfe0487bbc736327bed7377e1cb55`  
		Last Modified: Wed, 22 Apr 2026 02:17:11 GMT  
		Size: 55.2 MB (55170047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca40ab52301bb668be26e349c9d86d0f6bcd7bf48ed682080c62d66798e0b36e`  
		Last Modified: Wed, 22 Apr 2026 02:17:11 GMT  
		Size: 85.6 MB (85570480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5c9cabda3067bb97225b99ee52a16ce1b67adfee8209b73708702e0a988f42`  
		Last Modified: Wed, 22 Apr 2026 02:17:08 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b9eecfd6d1f53c043f4f1237ffcb6af565b3faba18412a91c6055f81d998ced9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7605878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2803afbf721024003c1384f1436e8f932288b96d1073f0f5d17dbeb99225f95c`

```dockerfile
```

-	Layers:
	-	`sha256:0785beff0119a77e21bca653d1b8878c14daaed6665ed16c6346da77bd3ab4ad`  
		Last Modified: Wed, 22 Apr 2026 02:17:08 GMT  
		Size: 7.6 MB (7591708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84675440e3cfe865de70ea7957a4b65b90b01376e13cc231d8969f87fdbb3ce6`  
		Last Modified: Wed, 22 Apr 2026 02:17:08 GMT  
		Size: 14.2 KB (14170 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d262c6cae15978a6d6ad22babc393a6545ed1bc8842a26ce426d794153631021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 MB (189304916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd893d2db8ba3cd1a4282874f0ffb6c514466b2a46fad88e6189b811da345da`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:19:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:19:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:19:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:19:10 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:19:10 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:20:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:20:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:20:14 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22606997067ab8451bc232fe95c1c369bdc4419b9cdae694d6baaed69249f329`  
		Last Modified: Wed, 22 Apr 2026 02:19:43 GMT  
		Size: 54.3 MB (54251621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b405c1fa7d6dcbefa61c6dd63658f4a9303077685ad59c8652352b3951d91f8`  
		Last Modified: Wed, 22 Apr 2026 02:20:33 GMT  
		Size: 85.4 MB (85383406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b13575e5decff1ee2209fed6d63c3198f59a925aaeef45371b3e6dfed33458`  
		Last Modified: Wed, 22 Apr 2026 02:20:31 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:af328245035b0c54b30749a7d99c9eba2e010e757ac0d9e75989b9a0ebde7595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7612926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a875ec18279f159ea506289e047c33cbf2411dd3118a3b365fc05dc8997412f`

```dockerfile
```

-	Layers:
	-	`sha256:5b21c735372bf0fa3d186f6f453b7e477a538e5f3768be8f28b438ef6625ef49`  
		Last Modified: Wed, 22 Apr 2026 02:20:31 GMT  
		Size: 7.6 MB (7599438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5b4b2b75322dc25460f22459c5b902f619e0b018b7ed91c64af76189d079b4d`  
		Last Modified: Wed, 22 Apr 2026 02:20:31 GMT  
		Size: 13.5 KB (13488 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:c0bb1194679eb58a2873511409766001b7aa9e111a8a3e76b8dfe0bdb7be3f2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 MB (196760402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e2fdb3a35a2099c97a825161cfa27ebe47e985b9c3a9fc09996083202202220`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 08:15:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 08:15:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 08:15:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 08:15:38 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 08:15:39 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 08:19:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 08:19:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 08:19:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0fab4f6170940889900b2327e1b3c62dace993eab8074ca7d33d1ffeef137c08`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 53.1 MB (53122984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40946bd06af436e9aec289d6d571e7a23a7c73218795b260867e8f81c9497e46`  
		Last Modified: Wed, 22 Apr 2026 08:16:57 GMT  
		Size: 52.7 MB (52650392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f41aab2e5d97f15ed30df40d0f5927cadec923366c2a60df9cc18d89760cd4d`  
		Last Modified: Wed, 22 Apr 2026 08:20:16 GMT  
		Size: 91.0 MB (90986382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d392a99dc148a2cc6dbea9062469749b22555f9f1a29364fca67309bb4dffbf0`  
		Last Modified: Wed, 22 Apr 2026 08:20:13 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:76e32adcda3bbfb08c74137175e3eb7de2b0e33b012a544ca1196efbbf93bb16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7610942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:326993c409c226fab0563ddb649e59eed12123af211c2d2df991c3f55301496b`

```dockerfile
```

-	Layers:
	-	`sha256:7512f265e1d7318fe3f7324787565736fcacc2cb4889b157e84a090327779bd6`  
		Last Modified: Wed, 22 Apr 2026 08:20:14 GMT  
		Size: 7.6 MB (7596724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:082f19142c58cd0b97133531fc918473e88f547b1a8bf319ab45d950a3fe74c4`  
		Last Modified: Wed, 22 Apr 2026 08:20:13 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json
