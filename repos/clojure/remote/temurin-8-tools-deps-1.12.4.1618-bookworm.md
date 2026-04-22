## `clojure:temurin-8-tools-deps-1.12.4.1618-bookworm`

```console
$ docker pull clojure@sha256:6b8044319b71fba436cf0cec33efcbb68299f2e959055a8597b2dcaf8c56bfff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.4.1618-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:9f71559044749915589d096d50b027f2835dc7317d6dbed3ed896a50970a4bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.8 MB (184825542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f88696c4e72c15501b6a25428dcf8c5241269cc529d3b31c690e3d18fe93598a`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:15:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:15:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:15:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:15:48 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:15:48 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:16:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:16:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:16:04 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c029e93bf248104e1b8930ad6e4a140e857057a59abbfdfb3066e57f15e98b`  
		Last Modified: Wed, 22 Apr 2026 02:16:24 GMT  
		Size: 55.2 MB (55170119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857d29c11b72ab2a0dad73968d552b9ca5374a1ac63438841caace09f07245c1`  
		Last Modified: Wed, 22 Apr 2026 02:16:24 GMT  
		Size: 81.2 MB (81166153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66bdd7b886095b6b4699aac6b8b2a56b230f63326f6ad4d38eea98000039b3f`  
		Last Modified: Wed, 22 Apr 2026 02:16:21 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:cac852ab72a0d011843818512d51863b039e9edc4afabc0b7b8da06aa271a661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d5b48849ca450eeebe3dc919bd24cef94cca0241637f45e407f4d75a38000f7`

```dockerfile
```

-	Layers:
	-	`sha256:64acb5e59ccdd2de1d8f58915ee9ed6cafed10a2c86905e515155603c7194221`  
		Last Modified: Wed, 22 Apr 2026 02:16:22 GMT  
		Size: 7.5 MB (7499289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7286433052525fc100fc1008c96f6c91ed87253b0b7264a2420dd9d721cb7967`  
		Last Modified: Wed, 22 Apr 2026 02:16:21 GMT  
		Size: 14.2 KB (14194 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1618-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:15ec3e70c8ebe5df2535dd1f236e52af0adeae6a9d85c5d78ef6c8048a90bf4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.8 MB (183798131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a3d87677f78ad16e4f41829f0064f484aaf503e8604ce9f7db75d3b3349cb0`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:19:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:19:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:19:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:19:21 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:19:21 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:19:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:19:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:19:37 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f76deade1e0f6edae9b3b77fb538c55d4effe3f4d174a1e6f818c3f2a24e50e`  
		Last Modified: Wed, 22 Apr 2026 02:19:55 GMT  
		Size: 54.3 MB (54251627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe3dfb76f1191e0955edbc628106fb21029bebccacdcbdbf588c69eb3b27302`  
		Last Modified: Wed, 22 Apr 2026 02:19:55 GMT  
		Size: 81.2 MB (81172789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d2d5b8165fb2becd9c738db40212b38c38c8ff06193caecce0ab58b8e6bfc5`  
		Last Modified: Wed, 22 Apr 2026 02:19:53 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f05ae09a99cf82f95628f8e91ec2b0552bd381e0991d46358969ab0c4c2c6422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7520064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68dbdc24d99b25083ab15c94a67664d43dbd62683634689279c462640ed16bdf`

```dockerfile
```

-	Layers:
	-	`sha256:ce5e283ff07f36b17db034deaf992177776418640d16d18b8b246743f834bcb7`  
		Last Modified: Wed, 22 Apr 2026 02:19:53 GMT  
		Size: 7.5 MB (7505752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:594ec03bbfd9fecbd1b862a00a927237e58655ca498b07b38d4ecd8a03f5f395`  
		Last Modified: Wed, 22 Apr 2026 02:19:52 GMT  
		Size: 14.3 KB (14312 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1618-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:3c73bd7e73d13309f17f3351146b30385bb42a8832e734684949f5b458d71fe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (191992088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e671240b2b4ad38427e92a9f64e37f3269799f683589e8f22cd473f7feaa946b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 02:30:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 02:30:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 02:30:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 02:30:35 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 02:30:35 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 02:35:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 02:35:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 02:35:02 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6b775f7ad22043f8bb75d535d8a1279e43453a08a4a9e6a0b48c020c9b387079`  
		Last Modified: Tue, 07 Apr 2026 00:09:43 GMT  
		Size: 52.3 MB (52336938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f15e3be605c892a466173dd560f0c76f39571ad77e4b26767f367028c3c142`  
		Last Modified: Thu, 16 Apr 2026 02:31:34 GMT  
		Size: 52.7 MB (52650392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0779b07ac8c2145154cfc45630fc2eefb647b37c24a9eef99c56d52f980ce3d`  
		Last Modified: Thu, 16 Apr 2026 02:35:36 GMT  
		Size: 87.0 MB (87004112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115e5f2db718facb3d084f2da591869bd9887a63e803e6601193e64c56eba780`  
		Last Modified: Thu, 16 Apr 2026 02:35:34 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4595f5032fd36f88d573c7909dce78dd372eaf8ae10277e45b7d3d91299f845f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7519342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e92eb7929093c1a39ecc3159ec3a8ea7152f9f36886ba6d81b68342a50ca699`

```dockerfile
```

-	Layers:
	-	`sha256:28443bdead56ad3aade83b4c91b7fb35a92d836e9f32c0a371e4088836158148`  
		Last Modified: Thu, 16 Apr 2026 02:35:34 GMT  
		Size: 7.5 MB (7505100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5034d444e413722c1b340de6d10ce31ba4a5394975b97f9bc564195a2296c97b`  
		Last Modified: Thu, 16 Apr 2026 02:35:34 GMT  
		Size: 14.2 KB (14242 bytes)  
		MIME: application/vnd.in-toto+json
