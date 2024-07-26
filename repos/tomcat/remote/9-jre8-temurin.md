## `tomcat:9-jre8-temurin`

```console
$ docker pull tomcat@sha256:a27d1bdb24733c8eded94d41d4e81c560c49a6c4a312da7a84458299a7410a05
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `tomcat:9-jre8-temurin` - linux; amd64

```console
$ docker pull tomcat@sha256:c985b7a5931b3125fd75f13e3d725ea3a74c97a0849ca2f41605bd8e595b8d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 MB (97856986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5345e014d55285f6e704672bf992ad72b59b836cb3ff2bcd3d35e3e9755714fa`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Mon, 08 Jul 2024 08:03:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Jul 2024 08:03:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 08:03:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 08 Jul 2024 08:03:40 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Mon, 08 Jul 2024 08:03:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0ac516cc1eadffb4cd3cfc9736a33d58ea6a396bf85729036c973482f7c063d9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='8fbefff2c578f73d95118d830347589ddc9aa84510200a5a5001901c2dea4810';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='13bdefdeae6f18bc9c87bba18c853b8b12c5442ce07ff0a3956ce28776d695ff';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='2991edbedee448c0f1edf131beca84b415dac64ea97365b9bfd85bc2f39893bb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Mon, 08 Jul 2024 08:03:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 08 Jul 2024 08:03:40 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 08:03:40 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
WORKDIR /usr/local/tomcat
# Mon, 08 Jul 2024 08:03:40 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 08 Jul 2024 08:03:40 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 08 Jul 2024 08:03:40 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 08 Jul 2024 08:03:40 GMT
ENV TOMCAT_MAJOR=9
# Mon, 08 Jul 2024 08:03:40 GMT
ENV TOMCAT_VERSION=9.0.91
# Mon, 08 Jul 2024 08:03:40 GMT
ENV TOMCAT_SHA512=b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948
# Mon, 08 Jul 2024 08:03:40 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Jul 2024 08:03:40 GMT
ENTRYPOINT []
# Mon, 08 Jul 2024 08:03:40 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708ff3b02f8b7b7711302f65e71cb2abbb60946f996f61dec11ce5788fc08f11`  
		Last Modified: Tue, 02 Jul 2024 06:00:37 GMT  
		Size: 12.9 MB (12871067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97aa4c2b7311ae2bf5d45bc877436e46ebc859b01d2cf63b66a3be9fa6ab8867`  
		Last Modified: Thu, 25 Jul 2024 17:27:24 GMT  
		Size: 41.9 MB (41884565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fdf9faa7f7d71b1e6168b61d171833e8e9dc3d56c7cc5100108961303ec9f8b`  
		Last Modified: Thu, 25 Jul 2024 17:27:20 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2e47ff4909e5589dd954ed48c76db5fcd454897fb4a03b27c06e73bbbcfeb0`  
		Last Modified: Thu, 25 Jul 2024 17:27:20 GMT  
		Size: 1.9 KB (1865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b86384ccae97cfd72e260e043c0d6b1c310763fd5ddd85029fd092e5bdec89a`  
		Last Modified: Thu, 25 Jul 2024 20:08:36 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df7234338c3edcf47d70577de4239d1b740fbb1827bcf767049357a3bba4e87`  
		Last Modified: Thu, 25 Jul 2024 20:08:38 GMT  
		Size: 12.4 MB (12441487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93303ee34c35590006459929a1eca7fd0c2e89f0de2dacd1d958c83248051eb4`  
		Last Modified: Thu, 25 Jul 2024 20:08:38 GMT  
		Size: 217.8 KB (217806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre8-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:20ca45a1804ef15de7c8588edf712a7751a1641d45f3cb53650bd2c802bea33a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d87cdd227267070ffe1249fa8085c105bcf019a5fb164de865e0b8de4c6ec9eb`

```dockerfile
```

-	Layers:
	-	`sha256:f8054ae4325eb3b0f66ecdd10201aa6d5c6f5e9cc799bbbc0ea5525a238a159f`  
		Last Modified: Thu, 25 Jul 2024 20:08:38 GMT  
		Size: 3.5 MB (3548678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89946d4037e6ca0f7217baa01fe85393dffaa92d175533b162e46aef6fded778`  
		Last Modified: Thu, 25 Jul 2024 20:08:37 GMT  
		Size: 23.7 KB (23725 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre8-temurin` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:089a0098229b784b9265f151f92be51b6a0ca94b3e1eab34af1ebf1a1fce7064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92149625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db13f1104f5ce19403a2a7d055195959a7c1c09b1b95e1136981ce0e07dfc78b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 27 Jun 2024 19:33:13 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:33:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:33:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:33:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:33:16 GMT
ADD file:967120bb21c0fbaf9bf6c8fcb7b292d31ec4812e538714e8beb0a6e013eae873 in / 
# Thu, 27 Jun 2024 19:33:16 GMT
CMD ["/bin/bash"]
# Mon, 08 Jul 2024 08:03:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Jul 2024 08:03:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 08:03:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 08 Jul 2024 08:03:40 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Mon, 08 Jul 2024 08:03:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0ac516cc1eadffb4cd3cfc9736a33d58ea6a396bf85729036c973482f7c063d9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='8fbefff2c578f73d95118d830347589ddc9aa84510200a5a5001901c2dea4810';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='13bdefdeae6f18bc9c87bba18c853b8b12c5442ce07ff0a3956ce28776d695ff';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='2991edbedee448c0f1edf131beca84b415dac64ea97365b9bfd85bc2f39893bb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Mon, 08 Jul 2024 08:03:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 08 Jul 2024 08:03:40 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 08:03:40 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
WORKDIR /usr/local/tomcat
# Mon, 08 Jul 2024 08:03:40 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 08 Jul 2024 08:03:40 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 08 Jul 2024 08:03:40 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 08 Jul 2024 08:03:40 GMT
ENV TOMCAT_MAJOR=9
# Mon, 08 Jul 2024 08:03:40 GMT
ENV TOMCAT_VERSION=9.0.91
# Mon, 08 Jul 2024 08:03:40 GMT
ENV TOMCAT_SHA512=b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948
# Mon, 08 Jul 2024 08:03:40 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Jul 2024 08:03:40 GMT
ENTRYPOINT []
# Mon, 08 Jul 2024 08:03:40 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e180e7b68e21ed1490bb8293a3e848136812456d07f1be0783ef04f773a97867`  
		Last Modified: Fri, 28 Jun 2024 02:10:28 GMT  
		Size: 27.5 MB (27534011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c3600b7820ccdab844af0b11c36a1aeadc460c5a3bc6a6fd0211a3fa9024fb1`  
		Last Modified: Tue, 02 Jul 2024 04:32:24 GMT  
		Size: 12.5 MB (12462968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34a319bcca6bbd9a3125b4c44c5968d12b16b481bdf3b06c3286f6f67ca5c06`  
		Last Modified: Thu, 25 Jul 2024 18:01:48 GMT  
		Size: 39.6 MB (39581667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8eb2726118f211dc250bd43b3c9bf05a6571b8b7e40675aef7e60800b48a07`  
		Last Modified: Thu, 25 Jul 2024 18:01:43 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9ec6f14a19bdcd141b3a5e419af4496a3785c1f122e5aad18ac4d1e2610ac9`  
		Last Modified: Thu, 25 Jul 2024 18:01:43 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ffe815ce82f879a9058e15779122f7c6cb3f461fb72cefcde73d460caa23f2`  
		Last Modified: Thu, 25 Jul 2024 20:39:21 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8fda53a5edb83381fd84d288664566f375c6e14040e07388631453be3ff75b`  
		Last Modified: Thu, 25 Jul 2024 20:39:21 GMT  
		Size: 12.4 MB (12377478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f79000c88ec0faeee076a93ee125a82563d20f485704c2b46b29612adb7a05`  
		Last Modified: Thu, 25 Jul 2024 20:39:21 GMT  
		Size: 191.3 KB (191303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre8-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:bb3829f25aefa189490d518c9076846f705a590cb35ec685f12e8ae1a0f53731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbaed4936f9790f1f716962a0d40e8046de6f8c154e0c963b04787f1f8a306f1`

```dockerfile
```

-	Layers:
	-	`sha256:70752639cedc447bb0473c519e23fb59985567f828f3c4eaa52c1b4236096ad7`  
		Last Modified: Thu, 25 Jul 2024 20:39:21 GMT  
		Size: 3.6 MB (3553148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33fd74996230e284bce2e76c987aeedc72ace7e25e5b4d96e4eac1ded741de30`  
		Last Modified: Thu, 25 Jul 2024 20:39:20 GMT  
		Size: 23.9 KB (23899 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre8-temurin` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:e8ec67851c9bc6effeb22d9abb856a4220b47b343f2724f9b9b0f4c633eee8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94738808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94031ce62b000c2a9b8b5b2a4489551a2ecd383922a6313e92e9fbf85a3284a`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Mon, 08 Jul 2024 08:03:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Jul 2024 08:03:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 08:03:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 08 Jul 2024 08:03:40 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Mon, 08 Jul 2024 08:03:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0ac516cc1eadffb4cd3cfc9736a33d58ea6a396bf85729036c973482f7c063d9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='8fbefff2c578f73d95118d830347589ddc9aa84510200a5a5001901c2dea4810';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='13bdefdeae6f18bc9c87bba18c853b8b12c5442ce07ff0a3956ce28776d695ff';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='2991edbedee448c0f1edf131beca84b415dac64ea97365b9bfd85bc2f39893bb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Mon, 08 Jul 2024 08:03:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 08 Jul 2024 08:03:40 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 08:03:40 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
WORKDIR /usr/local/tomcat
# Mon, 08 Jul 2024 08:03:40 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 08 Jul 2024 08:03:40 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 08 Jul 2024 08:03:40 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 08 Jul 2024 08:03:40 GMT
ENV TOMCAT_MAJOR=9
# Mon, 08 Jul 2024 08:03:40 GMT
ENV TOMCAT_VERSION=9.0.91
# Mon, 08 Jul 2024 08:03:40 GMT
ENV TOMCAT_SHA512=b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948
# Mon, 08 Jul 2024 08:03:40 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Jul 2024 08:03:40 GMT
ENTRYPOINT []
# Mon, 08 Jul 2024 08:03:40 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1598fb1bd1773a67ab2fadc579f10dd20c703a24f714a0df2c98f3475e0bdc58`  
		Last Modified: Thu, 25 Jul 2024 17:44:11 GMT  
		Size: 40.9 MB (40856858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866b82280e7b0d87170c7b588e4e7af85254d7215506084e35a43f9ff0b597a3`  
		Last Modified: Thu, 25 Jul 2024 17:44:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4542c70c56a320cea6f68915907a0f753fa4aab09c757c567654beb0b5018f90`  
		Last Modified: Thu, 25 Jul 2024 17:44:07 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852f9677a069754a26821869203a8a6fa7b24be388f438243389b365627637de`  
		Last Modified: Fri, 26 Jul 2024 02:24:18 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac3d80c084e2ba053777438974003c69f017226beccf26f05c6a65d5097f4e8`  
		Last Modified: Fri, 26 Jul 2024 02:24:19 GMT  
		Size: 12.4 MB (12448886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676f60090de0493a88bcdab7a903d1c9303c0772cce58df999cd4793b7b4c9e6`  
		Last Modified: Fri, 26 Jul 2024 02:24:18 GMT  
		Size: 216.8 KB (216774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre8-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:49130edc3aa56170b2ae001d2baad0b90cd98f6c59724c86954466c680787f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808f04154feedfbb07f68cabab70ffdc71c22d6954802e465648e28f259a4d61`

```dockerfile
```

-	Layers:
	-	`sha256:cbca06e381b7f82c94806eaa3c40a4b07f73458df5bd0bbca856cbca00e1fd7b`  
		Last Modified: Fri, 26 Jul 2024 02:24:19 GMT  
		Size: 3.5 MB (3549030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc8f0408f13116fadf0edf8715675331e66c12b437ae621766fcf3305ecad7b5`  
		Last Modified: Fri, 26 Jul 2024 02:24:18 GMT  
		Size: 24.4 KB (24441 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre8-temurin` - linux; ppc64le

```console
$ docker pull tomcat@sha256:041729764b0cb2c46a77857e9cb2372b9028271711335c72d639b1bbf25f8346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.3 MB (103269941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14515f1a181d087f652c71a8d82ca7727703c5780a394d9c31077e7a1bedd3cc`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Mon, 08 Jul 2024 08:03:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Jul 2024 08:03:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 08:03:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 08 Jul 2024 08:03:40 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Mon, 08 Jul 2024 08:03:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0ac516cc1eadffb4cd3cfc9736a33d58ea6a396bf85729036c973482f7c063d9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='8fbefff2c578f73d95118d830347589ddc9aa84510200a5a5001901c2dea4810';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='13bdefdeae6f18bc9c87bba18c853b8b12c5442ce07ff0a3956ce28776d695ff';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='2991edbedee448c0f1edf131beca84b415dac64ea97365b9bfd85bc2f39893bb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Mon, 08 Jul 2024 08:03:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 08 Jul 2024 08:03:40 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 08:03:40 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
WORKDIR /usr/local/tomcat
# Mon, 08 Jul 2024 08:03:40 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 08 Jul 2024 08:03:40 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 08 Jul 2024 08:03:40 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 08 Jul 2024 08:03:40 GMT
ENV TOMCAT_MAJOR=9
# Mon, 08 Jul 2024 08:03:40 GMT
ENV TOMCAT_VERSION=9.0.91
# Mon, 08 Jul 2024 08:03:40 GMT
ENV TOMCAT_SHA512=b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948
# Mon, 08 Jul 2024 08:03:40 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 08 Jul 2024 08:03:40 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Jul 2024 08:03:40 GMT
ENTRYPOINT []
# Mon, 08 Jul 2024 08:03:40 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8abbcd57d9001f5aade9e7c1c7cf47fea659efa1b67f1bf51c65e0f66569df0d`  
		Last Modified: Tue, 02 Jul 2024 02:09:14 GMT  
		Size: 35.6 MB (35588321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aea30364eff82eb5379f35c10575a54ece802a6af1763591c0a6a999d72c84c`  
		Last Modified: Tue, 02 Jul 2024 05:04:14 GMT  
		Size: 13.7 MB (13714876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e9ccd356c5e1cad719ae5b69ccb876cdfbca4bbd73249d42c85b5d90a124e2`  
		Last Modified: Thu, 25 Jul 2024 17:23:10 GMT  
		Size: 41.2 MB (41245886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a07f51bce2a67cb320b76536e85bcaf154e77c1bb68709790e74ba68daedb8b`  
		Last Modified: Thu, 25 Jul 2024 17:23:03 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311e39b7337ee73e6fd3a72eb90113c11c9f1437ed19ed32011fe2834f1acd3d`  
		Last Modified: Thu, 25 Jul 2024 17:23:03 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3cf415cd75f79a3e0ca4dcddf4168fd8b3dedf46423fdb4f2180194c061cfe`  
		Last Modified: Fri, 26 Jul 2024 00:12:38 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe4b89bda2989994bd4c48e20a3c93273fbb949b2074c0a4af3365431d1a20a`  
		Last Modified: Fri, 26 Jul 2024 00:12:39 GMT  
		Size: 12.5 MB (12469025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13b0dfa001945f928011a38dcddea540eb1f9cc54690305562b4a785fa7a9ab`  
		Last Modified: Fri, 26 Jul 2024 00:12:39 GMT  
		Size: 249.6 KB (249637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre8-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:6ed142c198dcf4fb9f95050d10940b9b57e1458b41d8d8855862635d74b32205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dffe1ebd5a5c23827a9558ac3597e23afb181bbf6a99b1bab9ab54db0ce5ab56`

```dockerfile
```

-	Layers:
	-	`sha256:1d0955a25c926fdff7c7779bcd29ff9d8927e39d41775864e041f8b237b84ef7`  
		Last Modified: Fri, 26 Jul 2024 00:12:39 GMT  
		Size: 3.6 MB (3553227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6fe9555bd99b709e6b45cad8a83b7e357d878d4c6c9e739c3f9a34324cbbf53`  
		Last Modified: Fri, 26 Jul 2024 00:12:38 GMT  
		Size: 23.8 KB (23825 bytes)  
		MIME: application/vnd.in-toto+json
