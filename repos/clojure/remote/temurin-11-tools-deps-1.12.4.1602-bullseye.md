## `clojure:temurin-11-tools-deps-1.12.4.1602-bullseye`

```console
$ docker pull clojure@sha256:3961413a4fdc018ab0d8a9d22dd72210252a20c1cbf3e8586ae24d7a7e9f5e39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.4.1602-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:d79f6a89facd959a4da7ad360ff03488d7ca01d621958cde6d6e488d7c107b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.3 MB (268265643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb4032515eed771aab64c13f01280b4ba70eba4ebf39ffed065578394a3f64f1`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Wed, 28 Jan 2026 18:03:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:03:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:03:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:03:36 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:03:36 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:03:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:03:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:03:49 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fccfc62cb15165379a658b98df1680b95e3908f69adc8e7176a095a7b4cf2106`  
		Last Modified: Tue, 13 Jan 2026 00:41:25 GMT  
		Size: 53.8 MB (53756446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3e99caca1c45bc46c394841237a9398a54a44d01423aa91758d77bfdaddf53`  
		Last Modified: Wed, 28 Jan 2026 18:04:11 GMT  
		Size: 145.0 MB (144966652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8832716f73c253b052c437ee876d2e1bcbe01417ef2af4909896e85e48d19592`  
		Last Modified: Wed, 28 Jan 2026 18:04:09 GMT  
		Size: 69.5 MB (69541899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a7a8eed21e8f9f51316f67c960bda941b7dc68f11b444dfadc409b846b6ad0`  
		Last Modified: Wed, 28 Jan 2026 18:04:06 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:ddd6cd127bfddf9f780fb46bafdb34a6d761fbe65c1bb438a0d4497ae9fdfd6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7430814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46eaf9b97562d9adeecf6e87f9f327b3e2b580fb3474c5b4d4c5a1d57e16609e`

```dockerfile
```

-	Layers:
	-	`sha256:7b390bcfe09c96ad16d536c02b5cf35a1c27c814ba661bb31905ab98643dffc7`  
		Last Modified: Wed, 28 Jan 2026 18:04:07 GMT  
		Size: 7.4 MB (7416607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6db4b5d931fb42ce3aabba0696be1ec1547e7da9bef09124298ed954d16100e6`  
		Last Modified: Wed, 28 Jan 2026 18:04:06 GMT  
		Size: 14.2 KB (14207 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1602-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5fbd2a553238d2d1ecfed0701b7c13db10c2f5a92c80ae969de638e14b8e89f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.7 MB (263681567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce07c951dd00b4cabb14f6966f8ba06bc0b2a1d29d9cbb52c47aff8ca397c617`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Wed, 28 Jan 2026 18:02:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:02:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:02:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:02:28 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:02:28 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:02:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:02:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:02:42 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:31 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d177e56bccd8f8b9c80c0ca2642da87f916ebd8b2999a27ce9dc1e4f75e9fc86`  
		Last Modified: Wed, 28 Jan 2026 18:03:05 GMT  
		Size: 141.7 MB (141729882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91bfd15949114e4715d7654255bad813fec7475d2cd49dba00d51f19b6e5bd0`  
		Last Modified: Wed, 28 Jan 2026 18:03:04 GMT  
		Size: 69.7 MB (69693270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee3837745f01bb64e1403116b3d12be1abd81db54935363c0ac60d8ea1e1014`  
		Last Modified: Wed, 28 Jan 2026 18:03:01 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d761189397a7fa70e43f70613d7f6d361a85ce2ad89345e6e12fd07806a15e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7436651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bedbeca4a1845644ebb12328291a0b109ee5dd85eb3c3937ce730a24d54c55a8`

```dockerfile
```

-	Layers:
	-	`sha256:64d55e6714c58e0c5ba9630effeaa3a77c0847a01b69c821b3221d8e8297b951`  
		Last Modified: Wed, 28 Jan 2026 18:03:02 GMT  
		Size: 7.4 MB (7422324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eccb0e26b50b04f00cc48bf96f05641304001b2491df9855cc03cc0643bf3303`  
		Last Modified: Wed, 28 Jan 2026 18:03:01 GMT  
		Size: 14.3 KB (14327 bytes)  
		MIME: application/vnd.in-toto+json
