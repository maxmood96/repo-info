<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:ce-6.1.0.3`](#aerospikece-6103)
-	[`aerospike:ee-6.1.0.3`](#aerospikeee-6103)

## `aerospike:ce-6.1.0.3`

```console
$ docker pull aerospike@sha256:1729ab9d4b7ebc59b82660f151c4ee67da243e6c560581304d55f008f8746bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ce-6.1.0.3` - linux; amd64

```console
$ docker pull aerospike@sha256:c5c73d707e2a698bb5a8d7a2a446d959f992e57b035c25922d41dca352c55c09
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65133858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7dfb346cd3f1f7ac12a79e23d465c5adde044266095080648a0ae84689197c`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-o","pipefail","-c"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:54 GMT
ADD file:1f1efd56601ebc26a041a7b994a380ef68112b91a078e225753bee7b3196d22c in / 
# Tue, 06 Dec 2022 01:20:54 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 01:44:06 GMT
ENV AEROSPIKE_VERSION=6.1.0.3
# Tue, 06 Dec 2022 01:44:30 GMT
ENV AEROSPIKE_SHA256=e4f9c152209547517951b78e42ca0251bd237fe1eba65b7bef81fea94ab653c9
# Tue, 06 Dec 2022 01:44:30 GMT
ENV AS_TINI_SHA256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940
# Tue, 06 Dec 2022 01:44:30 GMT
SHELL [/bin/bash -o pipefail -c]
# Tue, 06 Dec 2022 01:44:44 GMT
RUN export DEBIAN_FRONTEND=noninteractive   && apt-get update -y   && apt-get install -y --no-install-recommends     apt-utils     2>&1 | grep -v "delaying package configuration"   && apt-get install -y --no-install-recommends     binutils     ca-certificates     gettext-base     wget     xz-utils   && wget https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static --progress=bar:force:noscroll -O /usr/bin/as-tini-static 2>&1   && echo "$AS_TINI_SHA256 /usr/bin/as-tini-static" | sha256sum -c -   && chmod +x /usr/bin/as-tini-static   && wget "https://artifacts.aerospike.com/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian11.tgz" --progress=bar:force:noscroll -O aerospike-server.tgz 2>&1   && echo "$AEROSPIKE_SHA256 aerospike-server.tgz" | sha256sum -c -   && mkdir -p aerospike/pkg   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && ar --output aerospike/pkg -x aerospike/aerospike-tools-*.deb   && tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/   && rm -rf aerospike-server.tgz /var/lib/apt/lists/*   && dpkg -r apt-utils binutils ca-certificates wget xz-utils   && dpkg --purge apt-utils binutils ca-certificates wget xz-utils 2>&1   && apt-get purge -y   && apt-get autoremove -y   && find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike   && if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then     mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f /usr/lib/asadm/asinfo ]; then       ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;     fi   fi   && rm -rf /opt/aerospike/bin   && rm -rf aerospike
# Tue, 06 Dec 2022 01:44:44 GMT
COPY file:f497c4c6974a190f79a562efd9c9c0d6b753efe43e62c3fcc2536f74ad08238d in /etc/aerospike/aerospike.template.conf 
# Tue, 06 Dec 2022 01:44:44 GMT
COPY file:e3973656bf47d8e3796d7b5dc7200e68dcaedc877c80f4ebeed9484f3aa315d9 in /entrypoint.sh 
# Tue, 06 Dec 2022 01:44:45 GMT
EXPOSE 3000 3001 3002
# Tue, 06 Dec 2022 01:44:45 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 06 Dec 2022 01:44:45 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:025c56f98b679f70b7a54241917e56da7b59ab9d2defecc6ebdb0bf2750484bb`  
		Last Modified: Tue, 06 Dec 2022 01:25:12 GMT  
		Size: 31.4 MB (31412852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2d820c4e9f05f6fb9d2a8819ae7478a5e80b41693a3649822e72b531919198`  
		Last Modified: Tue, 06 Dec 2022 01:45:13 GMT  
		Size: 33.7 MB (33719199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e614ad6a0d8691fa7d4b47f47c3b57eae8d07e5bdde51d11f0761f8eef1015b`  
		Last Modified: Tue, 06 Dec 2022 01:45:08 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884d31ad4ac28cd0f8af70f5f861618c74a444483aaf2bfb727917c09b0f2726`  
		Last Modified: Tue, 06 Dec 2022 01:45:08 GMT  
		Size: 787.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:ee-6.1.0.3`

```console
$ docker pull aerospike@sha256:fbc7e95ed8411af9a4a80b1fbad3beb59b7f7fd07cf2dee91a24b82139ff8446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ee-6.1.0.3` - linux; amd64

```console
$ docker pull aerospike@sha256:a76e817762607a1774b5d34c82f4f1d4e7aefd4b7a7ee141c0a43a82746c2e74
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68170410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d99a17022b4e605916c2bf66a2275eb8e16ee30dfc5c903dc9d5b47a1e2cb15a`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-o","pipefail","-c"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:54 GMT
ADD file:1f1efd56601ebc26a041a7b994a380ef68112b91a078e225753bee7b3196d22c in / 
# Tue, 06 Dec 2022 01:20:54 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 01:44:06 GMT
ENV AEROSPIKE_VERSION=6.1.0.3
# Tue, 06 Dec 2022 01:44:06 GMT
ENV AEROSPIKE_SHA256=de62082abe7c5fb040fc5eaaed22274142d96cbcd7dfce7530a52d65bce8b277
# Tue, 06 Dec 2022 01:44:06 GMT
ENV AS_TINI_SHA256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940
# Tue, 06 Dec 2022 01:44:06 GMT
SHELL [/bin/bash -o pipefail -c]
# Tue, 06 Dec 2022 01:44:24 GMT
RUN export DEBIAN_FRONTEND=noninteractive   && apt-get update -y   && apt-get install -y --no-install-recommends     apt-utils     2>&1 | grep -v "delaying package configuration"   && apt-get install -y --no-install-recommends     binutils     ca-certificates     gettext-base     wget     xz-utils   && apt-get install -y --no-install-recommends     libcurl4     libldap-2.4.2   && wget https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static --progress=bar:force:noscroll -O /usr/bin/as-tini-static 2>&1   && echo "$AS_TINI_SHA256 /usr/bin/as-tini-static" | sha256sum -c -   && chmod +x /usr/bin/as-tini-static   && wget "https://artifacts.aerospike.com/aerospike-server-enterprise/${AEROSPIKE_VERSION}/aerospike-server-enterprise-${AEROSPIKE_VERSION}-debian11.tgz" --progress=bar:force:noscroll -O aerospike-server.tgz 2>&1   && echo "$AEROSPIKE_SHA256 aerospike-server.tgz" | sha256sum -c -   && mkdir -p aerospike/pkg   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && ar --output aerospike/pkg -x aerospike/aerospike-tools-*.deb   && tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/   && rm -rf aerospike-server.tgz /var/lib/apt/lists/*   && dpkg -r apt-utils binutils ca-certificates wget xz-utils   && dpkg --purge apt-utils binutils ca-certificates wget xz-utils 2>&1   && apt-get purge -y   && apt-get autoremove -y   && find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike   && if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then     mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f /usr/lib/asadm/asinfo ]; then       ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;     fi   fi   && rm -rf /opt/aerospike/bin   && rm -rf aerospike
# Tue, 06 Dec 2022 01:44:25 GMT
COPY file:f56e2e33c0b4bb66affff75053eaed44661e723b8b33d3ef3c10e305b506c350 in /etc/aerospike/aerospike.template.conf 
# Tue, 06 Dec 2022 01:44:25 GMT
COPY file:954d06187376ade36d0a4daf43c9abe4806362f2f33f0bd9dbaef5a67c967bd3 in /entrypoint.sh 
# Tue, 06 Dec 2022 01:44:25 GMT
EXPOSE 3000 3001 3002
# Tue, 06 Dec 2022 01:44:25 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 06 Dec 2022 01:44:25 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:025c56f98b679f70b7a54241917e56da7b59ab9d2defecc6ebdb0bf2750484bb`  
		Last Modified: Tue, 06 Dec 2022 01:25:12 GMT  
		Size: 31.4 MB (31412852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96234b1fe033779c03f491397e907d0f12736026c2297b5540692d779a13fd5`  
		Last Modified: Tue, 06 Dec 2022 01:45:01 GMT  
		Size: 36.8 MB (36755693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b41fd1d38b6c89354883c725319f6d3091120cadda1ec3508605cd970c450b`  
		Last Modified: Tue, 06 Dec 2022 01:44:56 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a75e93548d78a87f110d981fd558fe3617fcfb6f2d8b7642eff1d3a1047ebd1`  
		Last Modified: Tue, 06 Dec 2022 01:44:56 GMT  
		Size: 820.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
