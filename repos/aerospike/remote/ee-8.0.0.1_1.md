## `aerospike:ee-8.0.0.1_1`

```console
$ docker pull aerospike@sha256:d8877b15613d3855c86accf6f8ced2878207a5e20389466759e883848646d9a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-8.0.0.1_1` - linux; amd64

```console
$ docker pull aerospike@sha256:865c5b4aad460e8f1d25708e857b6d319d84313df1acbcbb667936805875122b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (82026241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9cc5384441d8bbf59d5f7f64272dd812bf49d5429634d6c324c91f537c51a87`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Thu, 23 Jan 2025 07:00:10 GMT
ARG RELEASE
# Thu, 23 Jan 2025 07:00:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 23 Jan 2025 07:00:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 23 Jan 2025 07:00:10 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 23 Jan 2025 07:00:10 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Thu, 23 Jan 2025 07:00:10 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 07:00:10 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.0.0.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Thu, 23 Jan 2025 07:00:10 GMT
ARG AEROSPIKE_EDITION=enterprise
# Thu, 23 Jan 2025 07:00:10 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.1/aerospike-server-enterprise_8.0.0.1_tools-11.2.0_ubuntu24.04_x86_64.tgz
# Thu, 23 Jan 2025 07:00:10 GMT
ARG AEROSPIKE_SHA_X86_64=25c2f8eb1bce53058419dfdba45ef25511e1419c2abf33fbf4547d66dca9bcb6
# Thu, 23 Jan 2025 07:00:10 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.1/aerospike-server-enterprise_8.0.0.1_tools-11.2.0_ubuntu24.04_aarch64.tgz
# Thu, 23 Jan 2025 07:00:10 GMT
ARG AEROSPIKE_SHA_AARCH64=eca17e36ec353d0da93228c2067b4a1524d8794385c8fd0b44da2b44b7445f51
# Thu, 23 Jan 2025 07:00:10 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Thu, 23 Jan 2025 07:00:10 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.1/aerospike-server-enterprise_8.0.0.1_tools-11.2.0_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=25c2f8eb1bce53058419dfdba45ef25511e1419c2abf33fbf4547d66dca9bcb6 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.1/aerospike-server-enterprise_8.0.0.1_tools-11.2.0_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=eca17e36ec353d0da93228c2067b4a1524d8794385c8fd0b44da2b44b7445f51
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Thu, 23 Jan 2025 07:00:10 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Thu, 23 Jan 2025 07:00:10 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Thu, 23 Jan 2025 07:00:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 23 Jan 2025 07:00:10 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Thu, 23 Jan 2025 07:00:10 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880858384eb1143c2212d5c048726ca030aed5cc9d13d8c5959587c3e91347bb`  
		Last Modified: Tue, 04 Feb 2025 04:37:05 GMT  
		Size: 52.3 MB (52269650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3470154a1dc7e61007194b1d75074402824ed3adab19c24258246dec4964a2a4`  
		Last Modified: Tue, 04 Feb 2025 04:37:04 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4468cb859db40368da5c3cd06a5fb5b043d9cc64e918628dae7a6cc8450e380`  
		Last Modified: Tue, 04 Feb 2025 04:37:04 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.0.0.1_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:67dda80c419693576a58f8e9de086fbb4d0f1b3d2b80725e6a7c8b390cc9f99f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1989320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4573dad95883f55e656bde96756d52ce4628fefe9acdcd6a089bcdc81001ca`

```dockerfile
```

-	Layers:
	-	`sha256:87a9b9d686cc3c31ac171ac775e494fe1380db13aaac61ff7627fcd29be95775`  
		Last Modified: Tue, 04 Feb 2025 04:37:04 GMT  
		Size: 2.0 MB (1960157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfe5e861f52850c1588e56c050503979241d85c8424c69f313082b5d9215a7b3`  
		Last Modified: Tue, 04 Feb 2025 04:37:04 GMT  
		Size: 29.2 KB (29163 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-8.0.0.1_1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:4ebcb0458f75761502b2803efe96fbb9413af8e50d5427cd8e633f2865a685c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80609248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f60f73509c155393ac152a419e50296458040098459ac0dfc83fd8e8eec9688`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Thu, 23 Jan 2025 07:00:10 GMT
ARG RELEASE
# Thu, 23 Jan 2025 07:00:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 23 Jan 2025 07:00:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 23 Jan 2025 07:00:10 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 23 Jan 2025 07:00:10 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Thu, 23 Jan 2025 07:00:10 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 07:00:10 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.0.0.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Thu, 23 Jan 2025 07:00:10 GMT
ARG AEROSPIKE_EDITION=enterprise
# Thu, 23 Jan 2025 07:00:10 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.1/aerospike-server-enterprise_8.0.0.1_tools-11.2.0_ubuntu24.04_x86_64.tgz
# Thu, 23 Jan 2025 07:00:10 GMT
ARG AEROSPIKE_SHA_X86_64=25c2f8eb1bce53058419dfdba45ef25511e1419c2abf33fbf4547d66dca9bcb6
# Thu, 23 Jan 2025 07:00:10 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.1/aerospike-server-enterprise_8.0.0.1_tools-11.2.0_ubuntu24.04_aarch64.tgz
# Thu, 23 Jan 2025 07:00:10 GMT
ARG AEROSPIKE_SHA_AARCH64=eca17e36ec353d0da93228c2067b4a1524d8794385c8fd0b44da2b44b7445f51
# Thu, 23 Jan 2025 07:00:10 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Thu, 23 Jan 2025 07:00:10 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.1/aerospike-server-enterprise_8.0.0.1_tools-11.2.0_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=25c2f8eb1bce53058419dfdba45ef25511e1419c2abf33fbf4547d66dca9bcb6 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.1/aerospike-server-enterprise_8.0.0.1_tools-11.2.0_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=eca17e36ec353d0da93228c2067b4a1524d8794385c8fd0b44da2b44b7445f51
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Thu, 23 Jan 2025 07:00:10 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Thu, 23 Jan 2025 07:00:10 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Thu, 23 Jan 2025 07:00:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 23 Jan 2025 07:00:10 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Thu, 23 Jan 2025 07:00:10 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59bc7d6678fa51a5f117719fb2c90387d40535bc2f25dba21c65d9c267169475`  
		Last Modified: Tue, 04 Feb 2025 08:58:54 GMT  
		Size: 51.7 MB (51713348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e75073328f1c3657ed86eead70ceb645849967bae8d0e4ca0487b352f68858`  
		Last Modified: Tue, 04 Feb 2025 08:58:52 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbafa24706a2ad5b7fd59c243888e5d6f9e4f69acadaa667f86dedcbe36fd13e`  
		Last Modified: Tue, 04 Feb 2025 08:58:52 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.0.0.1_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:6e6df59b4035b3afb3b0c931511315199d10567bd2fc208384c4844a178ce795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1991680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7476ccc31038b34a4f94e9fea534c028eea96438b94336a11149b4365856c0cc`

```dockerfile
```

-	Layers:
	-	`sha256:89847cca35b247cd209feef3678cdd8fc88b0ca75b21356d6758250186cb3a5d`  
		Last Modified: Tue, 04 Feb 2025 08:58:53 GMT  
		Size: 2.0 MB (1962437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3b466dd7657f4aeb44dd85bb32f09b09478e42259bbf2deb349c0684bf6467f`  
		Last Modified: Tue, 04 Feb 2025 08:58:52 GMT  
		Size: 29.2 KB (29243 bytes)  
		MIME: application/vnd.in-toto+json
