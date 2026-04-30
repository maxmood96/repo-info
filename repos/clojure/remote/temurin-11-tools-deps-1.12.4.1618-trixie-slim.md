## `clojure:temurin-11-tools-deps-1.12.4.1618-trixie-slim`

```console
$ docker pull clojure@sha256:8cbe3570796ad8e18200a11841bae5646e11d748d05b0f5f36c2c3f0158b38e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:39b000549ad28de70ae70067eed9be9678af92d4866e4802cb9a4a43645428de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.7 MB (247678111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92efb21470c7d90373e2b24fb3b3a2e3b8e6928d8de24728450c0513f1ca3807`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 29 Apr 2026 23:15:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:15:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:15:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:15:26 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 29 Apr 2026 23:15:26 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:15:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Apr 2026 23:15:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Apr 2026 23:15:41 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4e27bfc664b478706442369b1e3ae1c72634764abbe1b942aa05c54e0376c5`  
		Last Modified: Wed, 29 Apr 2026 23:16:01 GMT  
		Size: 145.9 MB (145886252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cdb3d86fbb64c14f29f6a66e826a259aed6ac96ce7b7e43b16b11f23a06c7ca`  
		Last Modified: Wed, 29 Apr 2026 23:16:00 GMT  
		Size: 72.0 MB (72011043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042e3814a56b935aea920e3021e2a766ff30280a7eba6b5e60d8e58aee91bfd1`  
		Last Modified: Wed, 29 Apr 2026 23:15:56 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4c5560c3c3b4338c08fd5f1d4f93188cb6b047767e5aa46c2062a8f58b857427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5293578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e857c57e41afc2c0fc32537ee87060e0544a35c3ea094aadabd424631304fa`

```dockerfile
```

-	Layers:
	-	`sha256:fb4ec4cade92e55579b93d380bfe49d89ba4496c8dd3dd9bd724650ef7db9b2a`  
		Last Modified: Wed, 29 Apr 2026 23:15:57 GMT  
		Size: 5.3 MB (5279335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f53ab099c6847d0cab03b555d808a4f2e9c1ed5b05030a856d9289cbef448f72`  
		Last Modified: Wed, 29 Apr 2026 23:15:56 GMT  
		Size: 14.2 KB (14243 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1771a312ec9b97245d32cdba171a246d7272385fd38e9a57fc42dd07539c1144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244558409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e87fe70a7d39dff7f83ee608fd50bb0117bead2c8c1783d5a2d329a41b423901`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 29 Apr 2026 23:15:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:15:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:15:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:15:06 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 29 Apr 2026 23:15:06 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:15:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Apr 2026 23:15:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Apr 2026 23:15:24 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1801e7e6c59434fe51af9529aabc7d1cd2d11a8dd491cc845496b49be42e0cc4`  
		Last Modified: Wed, 29 Apr 2026 23:15:48 GMT  
		Size: 142.6 MB (142583978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70909f2cdd3c7d39b9e6b4a094a68943791b747d929f34d4a1f619622bdd6223`  
		Last Modified: Wed, 29 Apr 2026 23:15:46 GMT  
		Size: 71.8 MB (71830181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aaf142f6e4e25ad353a06710aad705021d39e5eb882f0b8d4c3bf130cbad7b8`  
		Last Modified: Wed, 29 Apr 2026 23:15:43 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d6dd66c8bc7782ac27396ccad5117693132c6a690d0c03bea4f9ad14307988a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5300083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a17e64e7c4640008fe9b14e47a7c616de3b4b76994c19440454359c1ce1d0d53`

```dockerfile
```

-	Layers:
	-	`sha256:237353023256a2265de5233c83f15e94e08261eecaf07aa4438e93fa5ab943ad`  
		Last Modified: Wed, 29 Apr 2026 23:15:43 GMT  
		Size: 5.3 MB (5285722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e19e6c03a15cbb970b1c05885074eaf384dfba69065db653f47262c88286ccd6`  
		Last Modified: Wed, 29 Apr 2026 23:15:43 GMT  
		Size: 14.4 KB (14361 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:91d30b89afac8a8f50436ff4ab8a72484c64ae0bac375393c6d2f4afb524ed01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.0 MB (244024716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ac3f4fd31927d60df8a6b6b328da3fcd2760fb072699c212f8d43bedd9e553`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 08:22:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 08:22:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 08:22:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 08:22:31 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 08:22:35 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 08:27:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 08:27:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 08:27:39 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3730c515230ceba2109e879cebed0883fb00ea2c65355759d7c6c75f60fd28f2`  
		Last Modified: Wed, 22 Apr 2026 08:24:04 GMT  
		Size: 133.0 MB (132997390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8964f8415037c6647b4c48de7af8511251464f29bd25b6e3be99327f05248f8`  
		Last Modified: Wed, 22 Apr 2026 08:28:19 GMT  
		Size: 77.4 MB (77428652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca51bb7fb05b91c94f6a882a8d12d31bca2191f239835e08732b056fe10fa2d`  
		Last Modified: Wed, 22 Apr 2026 08:28:17 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c19dbfa9e76021e6e29549a13efe67704efecf5529d8da7ef51865d5eb3205e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7cd3a8b0923f656abe4588c366cd8bf1370de89cd106931259f10801429219c`

```dockerfile
```

-	Layers:
	-	`sha256:5bd404b77b2e4f1a249a207abc39d6d9a1ab2ba64a3b66a462ab237150a79aa2`  
		Last Modified: Wed, 22 Apr 2026 08:28:17 GMT  
		Size: 5.3 MB (5283089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ff6fa7a2e6d7eb606f0ce35406169fd69964e418f395b052f9d0a5ef5fffe86`  
		Last Modified: Wed, 22 Apr 2026 08:28:17 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:f0ba6eeb4e3c2218b6161558c4b9f67196bbf189da36439e3dc7a91f7b24410e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229480629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dc6291980099045523110cd30c4be0426619a4c31b3c727276b97486b7d5880`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 29 Apr 2026 23:14:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:14:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:14:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:14:16 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 29 Apr 2026 23:14:16 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:15:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Apr 2026 23:15:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Apr 2026 23:15:42 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aeee4edd1f5d8f782b9436601ddf2ffd14dd561b9e9b8c4a9f500a1b6f712e1`  
		Last Modified: Wed, 29 Apr 2026 23:14:54 GMT  
		Size: 126.7 MB (126652695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938a75217270f1acad48492680ccdaba86abd4f176f50ba96566f92aa0bee44e`  
		Last Modified: Wed, 29 Apr 2026 23:16:05 GMT  
		Size: 73.0 MB (72986990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d3a76967c889a97c56c7e30c3d2448d668f81bd10849d5aed96145d90c19e3`  
		Last Modified: Wed, 29 Apr 2026 23:16:04 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ef37bbeda4b3ea822faff82b9fe684f33ed63e664868a1ac615d2368084710d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b157754e64e5b5cda018da2bd4c3829c5fb97ff257db149cef1569fa0aa5df00`

```dockerfile
```

-	Layers:
	-	`sha256:838bc71f47c77c9a46ba33d96bb33b73ea56a3d96e5432a41b9ddf10b262721d`  
		Last Modified: Wed, 29 Apr 2026 23:16:04 GMT  
		Size: 5.3 MB (5275263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:616816bd1d38f2bbfcb9b9529fe3245757535b4b2c39a5b6561269713e13232a`  
		Last Modified: Wed, 29 Apr 2026 23:16:03 GMT  
		Size: 14.2 KB (14243 bytes)  
		MIME: application/vnd.in-toto+json
