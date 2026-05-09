## `clojure:temurin-11-bullseye`

```console
$ docker pull clojure@sha256:482a0c52ca386b1267a9deb22656ce3fbb7947854433454b5be3c660fde579ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:f6a0558d428ad4676ed0bdc42e4ffabd7916106eef224a23a9f0b1accb294e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269247743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea0185ea3e606d7f39a1f65ba238e22024f8bc634decbdaaf94b5d2dfa910da`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:16:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:16:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:16:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:16:29 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:16:29 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:16:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:16:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:16:43 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1c662d8f6b122c4f09d6ae1b210df55a5ba6e7b529807c0757ccba0c1ac508e0`  
		Last Modified: Fri, 08 May 2026 18:23:06 GMT  
		Size: 53.8 MB (53763343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc84c5f4eb17f33198800bc709b028992def83fe935b71dce48f7b012821384c`  
		Last Modified: Fri, 08 May 2026 20:17:06 GMT  
		Size: 145.9 MB (145886200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8537cfc4c669490651333d6fd4b60fa4e3c3138af30e0d6159f5a31676ae00`  
		Last Modified: Fri, 08 May 2026 20:17:05 GMT  
		Size: 69.6 MB (69597554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6114a6fedc715947c8dbfaacb7a76710796c525eca7f9418821bde0167c35ea`  
		Last Modified: Fri, 08 May 2026 20:17:02 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:17b69d637e7a4f62996bd74b6f41677944dd24eaefd04ea80e3951c6ecdd5c82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7442159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71e36cbef6d6e3053c2dd1abe73e8b241d18e8e448e7d159102a78c2c3ab0e10`

```dockerfile
```

-	Layers:
	-	`sha256:5cd1f69fb6d436bb6d35465b0df5749be540f92c7a5a9df79fce25ca7cecd15d`  
		Last Modified: Fri, 08 May 2026 20:17:02 GMT  
		Size: 7.4 MB (7427796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95235e988941a01c8f41d62d2b4313e72a922958b847530b8c281f227c7eefc7`  
		Last Modified: Fri, 08 May 2026 20:17:02 GMT  
		Size: 14.4 KB (14363 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5b9afe4811c6eca6d629d79f228ca0491fcfa0b459be3117bb7eb8973a4052a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.6 MB (264574643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60165ae6239290d112455c946b3f0d7231689dd1adec7fdcc7e7c86068e317e8`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:20:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:20:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:20:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:20:36 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:20:36 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:20:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:20:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:20:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6809e6326809787613a887bb088dd4863c66ee8ea3245fbf59b4929cd9c31831`  
		Last Modified: Fri, 08 May 2026 20:21:17 GMT  
		Size: 142.6 MB (142582223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77022f8535c307d9616ed28b4a3f089b5d7d3ebae43c3eab70d50c4800e918e`  
		Last Modified: Fri, 08 May 2026 20:21:16 GMT  
		Size: 69.7 MB (69738564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3717e33458b94e23528ad9cab845c0b7f25633a8db6143becf8f890656dac23`  
		Last Modified: Fri, 08 May 2026 20:21:13 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3db9a818ddf09d33527bf883a2b3185d82068b16e765c0b5c866f29746e1711b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7447994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0debb8e0b25371348fb1bb3acbd953c1a8203f99afd295a660499ad716c2161a`

```dockerfile
```

-	Layers:
	-	`sha256:6cc24bf19e3ccc05bd8abaf1f755edc716fe92a7114e238cdd3b22c2809c89d0`  
		Last Modified: Fri, 08 May 2026 20:21:13 GMT  
		Size: 7.4 MB (7433513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a17c5550d67abaecc53f7348c3263ffbe7a6dcdc9d504d16e6716f5d06a86909`  
		Last Modified: Fri, 08 May 2026 20:21:13 GMT  
		Size: 14.5 KB (14481 bytes)  
		MIME: application/vnd.in-toto+json
