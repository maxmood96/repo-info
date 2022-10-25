## `aerospike:ee-6.1.0.3`

```console
$ docker pull aerospike@sha256:17cca94ac289c55f4cd8849e7606caa2aa1be60078fe19f439937c2cc054fd56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ee-6.1.0.3` - linux; amd64

```console
$ docker pull aerospike@sha256:af4bd3a182179fe9ae6696b824eefdf2b00f33571078775404c40c1a149d265b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68177626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8191fc2fb180592c19b979f8661d5802e1cf69a5bd87f1b02eda449d712470cf`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-o","pipefail","-c"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:30:28 GMT
ENV AEROSPIKE_VERSION=6.1.0.3
# Tue, 25 Oct 2022 02:30:28 GMT
ENV AEROSPIKE_SHA256=de62082abe7c5fb040fc5eaaed22274142d96cbcd7dfce7530a52d65bce8b277
# Tue, 25 Oct 2022 02:30:28 GMT
ENV AS_TINI_SHA256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940
# Tue, 25 Oct 2022 02:30:28 GMT
SHELL [/bin/bash -o pipefail -c]
# Tue, 25 Oct 2022 02:30:46 GMT
RUN export DEBIAN_FRONTEND=noninteractive   && apt-get update -y   && apt-get install -y --no-install-recommends     apt-utils     2>&1 | grep -v "delaying package configuration"   && apt-get install -y --no-install-recommends     binutils     ca-certificates     gettext-base     wget     xz-utils   && apt-get install -y --no-install-recommends     libcurl4     libldap-2.4.2   && wget https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static --progress=bar:force:noscroll -O /usr/bin/as-tini-static 2>&1   && echo "$AS_TINI_SHA256 /usr/bin/as-tini-static" | sha256sum -c -   && chmod +x /usr/bin/as-tini-static   && wget "https://artifacts.aerospike.com/aerospike-server-enterprise/${AEROSPIKE_VERSION}/aerospike-server-enterprise-${AEROSPIKE_VERSION}-debian11.tgz" --progress=bar:force:noscroll -O aerospike-server.tgz 2>&1   && echo "$AEROSPIKE_SHA256 aerospike-server.tgz" | sha256sum -c -   && mkdir -p aerospike/pkg   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && ar --output aerospike/pkg -x aerospike/aerospike-tools-*.deb   && tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/   && rm -rf aerospike-server.tgz /var/lib/apt/lists/*   && dpkg -r apt-utils binutils ca-certificates wget xz-utils   && dpkg --purge apt-utils binutils ca-certificates wget xz-utils 2>&1   && apt-get purge -y   && apt-get autoremove -y   && find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike   && if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then     mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f /usr/lib/asadm/asinfo ]; then       ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;     fi   fi   && rm -rf /opt/aerospike/bin   && rm -rf aerospike
# Tue, 25 Oct 2022 02:30:47 GMT
COPY file:f56e2e33c0b4bb66affff75053eaed44661e723b8b33d3ef3c10e305b506c350 in /etc/aerospike/aerospike.template.conf 
# Tue, 25 Oct 2022 02:30:47 GMT
COPY file:954d06187376ade36d0a4daf43c9abe4806362f2f33f0bd9dbaef5a67c967bd3 in /entrypoint.sh 
# Tue, 25 Oct 2022 02:30:47 GMT
EXPOSE 3000 3001 3002
# Tue, 25 Oct 2022 02:30:47 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 25 Oct 2022 02:30:47 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5093ffd22d77551e6ca3b91a084e5e6f075b404fadd2cd9f4d7a0942c3151b51`  
		Last Modified: Tue, 25 Oct 2022 02:31:23 GMT  
		Size: 36.8 MB (36755723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda274c3d52f6898d0962fed9fb8dc831e5256839fea6dcb9aa59204dcb87f6a`  
		Last Modified: Tue, 25 Oct 2022 02:31:18 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3205cb68ed5d8349118e4d1ed1dc01e1d643cd127dcbd772c765fbf845008050`  
		Last Modified: Tue, 25 Oct 2022 02:31:18 GMT  
		Size: 821.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
