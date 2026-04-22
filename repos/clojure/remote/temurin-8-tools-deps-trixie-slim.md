## `clojure:temurin-8-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:9d65ad4307d4fe03cfa914c6f72bb307aad1dabfd9042dbef853e8b5f129c27a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9fd08bc8f0d8772adfa47129f7fb3fea1787ca1838233ec9c4c3245d30a0ed77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (156961829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992fa6027cb822fa5fcc79707b50d2b722299bcb37db400b31a91841a7fdefa8`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:16:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:16:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:16:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:16:27 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:16:27 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:16:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:16:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:16:43 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d1cae898dc1c04534e248bfe4259fbff5a89a5f96ebf1ff9f3b42ec9919255`  
		Last Modified: Wed, 22 Apr 2026 02:16:59 GMT  
		Size: 55.2 MB (55170060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5958b5ff669cfcf59a2a79b045d9a5c9e732ca9412d875e246e150c5a471b13`  
		Last Modified: Wed, 22 Apr 2026 02:17:00 GMT  
		Size: 72.0 MB (72010949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62eaf8576af3941ed440c100c95089d34dcfbdd6a03e89cfbacd65b92d9efcd`  
		Last Modified: Wed, 22 Apr 2026 02:16:57 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0efc7a23b9ecb3aebcb6cb9b0da58a5b4c546fc815649e0e11f70f065b772076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5394406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9278383163f54f80ead043984c593a70c8c4e2ad12d5bd7cfa5d947707a2f73`

```dockerfile
```

-	Layers:
	-	`sha256:8ca518f4fe73fe0eddd323374456eae1f062ac5f74a8e6fe42aa7ad13dae2696`  
		Last Modified: Wed, 22 Apr 2026 02:16:57 GMT  
		Size: 5.4 MB (5380179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce4cb9387b375d794bf21021880d6bf9e1b48839cf524b7331e8a4f391a48a63`  
		Last Modified: Wed, 22 Apr 2026 02:16:57 GMT  
		Size: 14.2 KB (14227 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:02afec29b29ce9ce6a672bc6281bbb4dbba769e16cc812b18c713356dfeffb2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156226847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eff34de459faa979c85a2f2bd43b846ef7a2aea0fb3b82535670fc2c1d47810`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:20:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:20:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:20:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:20:05 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:20:05 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:20:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:20:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:20:23 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e628327cefc23b092dca20ecb6169d1e4c94a5ee584ac50dee57220c6822178`  
		Last Modified: Wed, 22 Apr 2026 02:20:40 GMT  
		Size: 54.3 MB (54251614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33848781087c919a9ba6398a5035322a23449f5012defe7a985efcdd1a069b80`  
		Last Modified: Wed, 22 Apr 2026 02:20:41 GMT  
		Size: 71.8 MB (71830984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330d0fd76f9c9891d9fc57101417522541597da1420ec2addb9990660d43aa2b`  
		Last Modified: Wed, 22 Apr 2026 02:20:38 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9a4025fb4c0447de274ea1a5a3eeb4761f2f87784fa3e5cb7e8165cd1ce6d00a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5400994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50a5feab113742a7d5ca7517f82bfe2db27133edca44b107ebecf9927d1c0c53`

```dockerfile
```

-	Layers:
	-	`sha256:7d62de61dec13be911a607d58ac141f350243b68a81975aa6c59b492ecd1236c`  
		Last Modified: Wed, 22 Apr 2026 02:20:38 GMT  
		Size: 5.4 MB (5386648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdb6017918db21622edfeca99f2681a3891f58f745768d84b74272275d74b3f2`  
		Last Modified: Wed, 22 Apr 2026 02:20:38 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:acfb46e07f62ece96a2c337e3382bbb811c12b1cae22530fed90fcd3794d9801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163677454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a95b748d55adb5b97916f1d1c48daa13436066162f738bc4fe14b9aac431a88c`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 08:16:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 08:16:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 08:16:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 08:16:14 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 08:16:17 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 08:19:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 08:19:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 08:19:41 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909dacfd29690d1229d823bbdff4948ce65ffd405125b5cb14537992f61a0959`  
		Last Modified: Wed, 22 Apr 2026 08:17:19 GMT  
		Size: 52.7 MB (52650391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f0c74378f2b29f7d9fa383a3cbcc484f21fc13e9a77b3c29d6d74c784ae14a`  
		Last Modified: Wed, 22 Apr 2026 08:20:16 GMT  
		Size: 77.4 MB (77428387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1a539cb8410f6939bd9d31b654e493435300a31d4717968d1ae3b15584cde6`  
		Last Modified: Wed, 22 Apr 2026 08:20:13 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:384f5f811c780240d0031972e2facdfb3a75a06b2f97aac5e67bc6b5af028f01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5399421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f723c696e988d8bac469db7d55c2f5641a05d28b708a57ea9ec3576826a07add`

```dockerfile
```

-	Layers:
	-	`sha256:fabebc9ab7f51a545ee41a9d57c6d0f53e6596de3c5cd63455d07ff159a3423f`  
		Last Modified: Wed, 22 Apr 2026 08:20:14 GMT  
		Size: 5.4 MB (5385145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:970b1fc2a9b2eabe8cfb73b4f3b67a8731b65298abe2f0b2f79162b0437a31d7`  
		Last Modified: Wed, 22 Apr 2026 08:20:13 GMT  
		Size: 14.3 KB (14276 bytes)  
		MIME: application/vnd.in-toto+json
