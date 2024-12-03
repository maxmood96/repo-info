## `clojure:temurin-21-bullseye-slim`

```console
$ docker pull clojure@sha256:b8210b421d908df4ac9eb99cc317582300bfb0491fe355a63dee3e432bfc840e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d92b4711af0dd90eb26655722362795b066b476dd71cc759e8ed49119ec60692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246578452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2486127f68bca8e2b7ef333797376ad4d0151b8ea1b2c8976c54aadb7190962e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa1805c88fab089f4a11f055d0117232de7b7a3dbaaa6643c5367734a6b6011`  
		Last Modified: Tue, 03 Dec 2024 03:25:51 GMT  
		Size: 157.6 MB (157568673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6576be0474378ecc84e5189b8d9024c54ca7156273ee08a00edb55a6e8d15f`  
		Last Modified: Tue, 03 Dec 2024 03:25:50 GMT  
		Size: 58.8 MB (58756100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fad9a7c4b3ea6c8cf650b9e5ecc428d17a181894a098567494ebbfe5b6fd4f2`  
		Last Modified: Tue, 03 Dec 2024 03:25:49 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44886777db8be53659781a1f3e8874734adc0730884ff4c0196ff68022a49323`  
		Last Modified: Tue, 03 Dec 2024 03:25:49 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f6237803d26fa4a5d28d4369c8ad42786be7c7973d4aed7ea776d597d5f9fc6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5143927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7bd3472bb9c3be6473dc81b1aca2800edd71544380e28f654114ab33b5d4a8e`

```dockerfile
```

-	Layers:
	-	`sha256:9461e54a2b3cf62754e0c892df04a5c5db6bd33b8187123490260a0fc1d12984`  
		Last Modified: Tue, 03 Dec 2024 03:25:49 GMT  
		Size: 5.1 MB (5127352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65ac9036a11194519edbdbceb173166b6e8007a84b58e10a3a660f659badbb16`  
		Last Modified: Tue, 03 Dec 2024 03:25:49 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f8e40e76107888f118ea46cf1e8f2f73850e20a3ca586e18447bdee846ca6080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.8 MB (244761234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea9f619e1088f5668b4db3a47f8152192cf2081321e21d3be5f6c721cafba2d8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65761880f0d53d3a20a6b437a7598675ca1a3cb59cca575f1ee410b546862a1a`  
		Last Modified: Sat, 16 Nov 2024 05:40:31 GMT  
		Size: 155.8 MB (155793069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8ad42f9046999e51a6eae35e00b5b57e0b0f83550db81023febb679d71c090`  
		Last Modified: Sat, 16 Nov 2024 05:44:42 GMT  
		Size: 58.9 MB (58875525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed941461d5f6fa9502e8ee73e3aec39da8f9d73d982a9d53d3726b5a629be4a`  
		Last Modified: Sat, 16 Nov 2024 05:44:40 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75325a85f4f9268abb6b3b864ed4621d57651bc4d3ad856cc7cc05a3a29335f`  
		Last Modified: Sat, 16 Nov 2024 05:44:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:96e589d77dda2905362ef89da35bc74942dbbf92473f43b43a237e1539f768a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5151633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7baa7b75dc40c752a709016510797127e910c04735e673693283e5fe265c6481`

```dockerfile
```

-	Layers:
	-	`sha256:53c7d0b542a3e076a2e548454d8c3372e47d4c18c915dd1e46305c3d3687e15c`  
		Last Modified: Sat, 16 Nov 2024 05:44:41 GMT  
		Size: 5.1 MB (5134916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:332d6ac67d77c49698bf1840cb6423cd6cd99225d22e74fa41e6176112c7cbe8`  
		Last Modified: Sat, 16 Nov 2024 05:44:40 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
