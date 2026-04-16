## `clojure:temurin-8-tools-deps-1.12.4.1618-bookworm`

```console
$ docker pull clojure@sha256:16d70089f6cdecb79114d78853ebcf9e572ab7fa36d30a687ee90f266a17276d
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
$ docker pull clojure@sha256:3104609836fb8e0045ec526d184f258782b8d11155db315e9b99428cc0108afa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.8 MB (184826127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806ad2ac156c95a4a9833b48825052bfc65433481bc5a93b2edef24f3b2022e9`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:00:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:00:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:00:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:00:29 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:00:29 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:01:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:01:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:01:44 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f4ed036afffbee859ae4915feeef010e92bff8b7b13abb39ca803dfe51a8dc`  
		Last Modified: Wed, 15 Apr 2026 22:01:01 GMT  
		Size: 55.2 MB (55170060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb2fbc54b81fe59fe2f837922e6c12c5bb93a26b47b13291d2cd83000023f3c`  
		Last Modified: Wed, 15 Apr 2026 22:02:01 GMT  
		Size: 81.2 MB (81166598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f476aa088c8b874abdde5d507d1967e2ab49fc0e2b7d1d2048bf7feef0f569`  
		Last Modified: Wed, 15 Apr 2026 22:01:59 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1fcf387a146e1b2705440d80ae3dc2731d837f83edd0c7f3e07076f46ebdc873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:660349ae1eaca0a17451a6683e0f42a480cad2c1fc7b30dfb1c9facbc697b7fc`

```dockerfile
```

-	Layers:
	-	`sha256:ec839470b9823ecd956553e0048a009bb577de21f6b358c387a2b25c99264275`  
		Last Modified: Wed, 15 Apr 2026 22:01:59 GMT  
		Size: 7.5 MB (7499289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a738ad7151f47b7293d87ba2669c886d477c30afecb095af1cf8f6fbed4cb5fe`  
		Last Modified: Wed, 15 Apr 2026 22:01:59 GMT  
		Size: 14.2 KB (14194 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1618-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c8107769554aac22198a9b253de204db1211931a1491990922be3efcf479fdc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.8 MB (183798508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36ae345710df2557fdac421c9db5c4c5108f1c6a1609e90f872930573a86008c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:12:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:12:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:12:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:12:49 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:12:49 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:13:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:13:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:13:05 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c5ef4171512b9c399c04b97ff10c48058a8756dd9ed900cc7174e46fd73783`  
		Last Modified: Wed, 15 Apr 2026 22:13:26 GMT  
		Size: 54.3 MB (54251612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482fa37c63ecce13b9380d24e748450fe39d120e0942756ccde08b63775f7774`  
		Last Modified: Wed, 15 Apr 2026 22:13:32 GMT  
		Size: 81.2 MB (81172988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48474326a048f4d15fe4e4d0c48e2b4f820b65814ce79d6082c6e247c9ab68c`  
		Last Modified: Wed, 15 Apr 2026 22:13:24 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:50f3cbc7c87152f7cc1a891be63f5021e4fddd58cd3b6f0fb268f9073d9bcd87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7520064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53d70e098dacb43f04088ba88cfcb7a29d5db12e8df4c80c55e1925caea8c5f`

```dockerfile
```

-	Layers:
	-	`sha256:b1076e7ab60c8c977676e8e41d28b650a721ee794970e329257acdb1097e5929`  
		Last Modified: Wed, 15 Apr 2026 22:13:24 GMT  
		Size: 7.5 MB (7505752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9aecdfd3db29e6a9422de30e637e8a2619aa6dc89204bc50e3a5d35a809864e3`  
		Last Modified: Wed, 15 Apr 2026 22:13:23 GMT  
		Size: 14.3 KB (14312 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1618-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:3ca893fac50444059f0bb188fd7adf7bb47c861236ad16a16db9f476af149a1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (191988083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0296d64a783b24de83f67d224ecd58d94e23d78435895718d2f5033b9059cf7c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 14:20:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:20:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:20:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:20:05 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 14:20:06 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:25:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 14:25:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 14:25:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6b775f7ad22043f8bb75d535d8a1279e43453a08a4a9e6a0b48c020c9b387079`  
		Last Modified: Tue, 07 Apr 2026 00:09:43 GMT  
		Size: 52.3 MB (52336938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198aa8af97ba5b55cc83e5b59bee258e24a99d12a6acfe2745f351375cceb0d5`  
		Last Modified: Tue, 07 Apr 2026 14:21:35 GMT  
		Size: 52.7 MB (52650379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe291cdbac7c00f0e0bc40b402deb914bae67a872addc06eaf1dc82b8775b220`  
		Last Modified: Tue, 07 Apr 2026 14:26:18 GMT  
		Size: 87.0 MB (87000120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4bf5f95fcd625c2f43b4570bb1419e782a2120a4209e294f9e26cdfdd699ac`  
		Last Modified: Tue, 07 Apr 2026 14:26:16 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:3f982cde526be275f9dc849ff659c7bfc581fd3f5618c1cc8ce23a318bfb69b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7519342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d95290d6b3a78d0028e2fd0d67a0fa5a089325b4cc73a15c0a99995381ea246`

```dockerfile
```

-	Layers:
	-	`sha256:31d73c353d597bba20cdc593392a84b9b39a21a3ff1666878e6f4f2e3d9d2eef`  
		Last Modified: Tue, 07 Apr 2026 14:26:17 GMT  
		Size: 7.5 MB (7505100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce0465152aeb4151a48502cab8c5029e42d721234d12497289aee7f7326b239d`  
		Last Modified: Tue, 07 Apr 2026 14:26:16 GMT  
		Size: 14.2 KB (14242 bytes)  
		MIME: application/vnd.in-toto+json
