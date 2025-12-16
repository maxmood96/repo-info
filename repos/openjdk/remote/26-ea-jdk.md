## `openjdk:26-ea-jdk`

```console
$ docker pull openjdk@sha256:f1ca58b65730b9ec4431f768bcbc732ade5c015e630f9c5015d0e3781e08dae8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `openjdk:26-ea-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:0a70b1422e6db123e9f0da34821495286ad31e76ce7265df2ad2a36ea9fd644e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.4 MB (313431891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ee96a7d88c7194a414e98b81e9e7dc146ae1e12b980b4115383a696f14133d8`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:31 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:31 GMT
CMD ["/bin/bash"]
# Tue, 16 Dec 2025 00:02:35 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 16 Dec 2025 00:02:45 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Tue, 16 Dec 2025 00:02:45 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 00:02:45 GMT
ENV LANG=C.UTF-8
# Tue, 16 Dec 2025 00:02:45 GMT
ENV JAVA_VERSION=26-ea+28
# Tue, 16 Dec 2025 00:02:45 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/28/GPL/openjdk-26-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='a18910b0bdceb12a4f78147a1feebee50cc621ad8114c07a1ab071e58c17b09d'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/28/GPL/openjdk-26-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='d330a706e3fc611f4b39f6768f104e47d0a755ffabda31e3299dbc2e791f4f18'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Dec 2025 00:02:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7a5e1e9175268f8a5062cd666fcd7ea2d50d08a02f6eb1873586009eb9e27529`  
		Last Modified: Tue, 02 Dec 2025 21:17:55 GMT  
		Size: 47.3 MB (47314748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795be9687a89d72dfa96f36a2dc857ace42392b9e386013f4dbead076eb8b220`  
		Last Modified: Tue, 16 Dec 2025 00:03:32 GMT  
		Size: 38.3 MB (38297199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c000f7227ee778d29e004e46e3a94923fe49576866652dfb883e0f127f901d`  
		Last Modified: Tue, 16 Dec 2025 00:03:40 GMT  
		Size: 227.8 MB (227819944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:3570ce40cd3532996bfea0ed9ff6d1e6de764e2028ae523ddc65d7125bdb4099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:383028a4bb98c917656ae722244bc58112f144be4446b743768902416efa58a9`

```dockerfile
```

-	Layers:
	-	`sha256:8f900582b30481f5c1adc480401e399c4b92eb25d256c2bf86c6f615fa255bd6`  
		Last Modified: Tue, 16 Dec 2025 01:23:26 GMT  
		Size: 3.7 MB (3655331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4d6d9e2ae1a1998c111159edb53c415f76c3150f04a0eb85b469d3d2c8ca244`  
		Last Modified: Tue, 16 Dec 2025 01:23:27 GMT  
		Size: 17.8 KB (17839 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6f1ff89e8557ab814aa24d28950f80afaf487a7febfe15ff3673e89c4ad5c343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.3 MB (310331810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee7143b634beb64397204c89ee04b3ff54e6f7e4adc1cb0a538c2b8feb473a79`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:01 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:01 GMT
CMD ["/bin/bash"]
# Tue, 16 Dec 2025 00:02:24 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 16 Dec 2025 00:02:45 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Tue, 16 Dec 2025 00:02:45 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 00:02:45 GMT
ENV LANG=C.UTF-8
# Tue, 16 Dec 2025 00:02:45 GMT
ENV JAVA_VERSION=26-ea+28
# Tue, 16 Dec 2025 00:02:45 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/28/GPL/openjdk-26-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='a18910b0bdceb12a4f78147a1feebee50cc621ad8114c07a1ab071e58c17b09d'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/28/GPL/openjdk-26-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='d330a706e3fc611f4b39f6768f104e47d0a755ffabda31e3299dbc2e791f4f18'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Dec 2025 00:02:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:842b90544a0050f7b114b301fe9bf455545f1ec7b827c2f9ec9585171d12c48f`  
		Last Modified: Tue, 02 Dec 2025 21:17:32 GMT  
		Size: 45.9 MB (45897032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc939c9928182a9c75221b9568a63a4fe7499d89f832ead56b8ea289392e8e0`  
		Last Modified: Tue, 16 Dec 2025 00:03:32 GMT  
		Size: 38.7 MB (38700187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f65678c1ac0e7dc12c615167283fe402abaca32375a7efd2db08fd51547969`  
		Last Modified: Tue, 16 Dec 2025 00:03:41 GMT  
		Size: 225.7 MB (225734591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:5efd71de9edfe6a852d5a8c083921b74efb0eb3f4d5d4c544ebe295f15f8bc30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f9601468582e3586d0029648f81c53e255f6acc93345784c80810135ba010fa`

```dockerfile
```

-	Layers:
	-	`sha256:817441da23b2e606e20ec2602f6dd2e6017cbe6f509cf5d864cd449f0683e8e6`  
		Last Modified: Tue, 16 Dec 2025 01:23:31 GMT  
		Size: 3.7 MB (3653021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bf14522b56929cfb752915cde0e0732581cb24a139351f2a406a9b60d26f73a`  
		Last Modified: Tue, 16 Dec 2025 01:23:32 GMT  
		Size: 18.1 KB (18054 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk` - windows version 10.0.26100.7462; amd64

```console
$ docker pull openjdk@sha256:6e380ee6580cbd135db09b1af1379d4ff9aa7652479f7b9908c01077cd70a14d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3478068626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd0b7dd5f3ca81971103e2774dd4edebde69a5ff60d022a4e314c2d4c7dfb9d7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Tue, 16 Dec 2025 00:11:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Dec 2025 00:11:16 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 16 Dec 2025 00:11:16 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 16 Dec 2025 00:11:23 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 16 Dec 2025 00:11:24 GMT
ENV JAVA_VERSION=26-ea+28
# Tue, 16 Dec 2025 00:11:24 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/28/GPL/openjdk-26-ea+28_windows-x64_bin.zip
# Tue, 16 Dec 2025 00:11:25 GMT
ENV JAVA_SHA256=1043a56a8e09613f76543d6e9290ff5c53e9cc2bcf0053550a36ad993843bf2c
# Tue, 16 Dec 2025 00:11:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 16 Dec 2025 00:11:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890b21ccebaeedf053c6c32fb4fe8d98ab2c60496b12e6b730ac67df9096fc5b`  
		Last Modified: Tue, 09 Dec 2025 19:44:14 GMT  
		Size: 1.0 GB (1037813290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9084b4fcbb7315770c061c935d37e934db4808ffa39e15e2ecc7a0f7dcf310`  
		Last Modified: Tue, 16 Dec 2025 00:31:21 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468acb3cc160814c9d78adbad78b2d34a2f5c5ffc8c1d3339a297f665ec5946b`  
		Last Modified: Tue, 16 Dec 2025 00:31:21 GMT  
		Size: 375.9 KB (375885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516491c030339ab52bc666c0c0e2008f0e3ec3fc6e2eab8a86c799fea34d8a6e`  
		Last Modified: Tue, 16 Dec 2025 00:31:21 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db446e317c732404081228a000c3aa7352b4307154946e9de963d5eadd277952`  
		Last Modified: Tue, 16 Dec 2025 00:31:21 GMT  
		Size: 355.8 KB (355808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cca07bac0163fce108a133a8e3929a7ebd5b66275654019d73bb99a90484546`  
		Last Modified: Tue, 16 Dec 2025 00:31:21 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b306042d000ce09fe72db3ffb884f0f0d068cb4fd7f08b150e92351d7a39e61b`  
		Last Modified: Tue, 16 Dec 2025 00:31:21 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3975ff4b0d611f284714f5c3836b95ad116395395dc7db55bfa08ee0d108eedf`  
		Last Modified: Tue, 16 Dec 2025 00:31:21 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deaec69ef65eee456b230a03487572c2976bc5fc4617beadd78b25bdee36951b`  
		Last Modified: Tue, 16 Dec 2025 00:33:22 GMT  
		Size: 224.2 MB (224208611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c866f01fdc92561b370b57406361d24b13ab0c04e4b76d4eb5a8bedf0340d4b`  
		Last Modified: Tue, 16 Dec 2025 00:31:21 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-ea-jdk` - windows version 10.0.20348.4529; amd64

```console
$ docker pull openjdk@sha256:e1646488a9b1b10d5ff28a2f5e166c5ce53caa04fdb864c9ae7a34c959c79893
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2004956527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb65ec2b9eff1a3203ea84526164e3d2202ca4e168572f16363ebb0ba5722ade`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 16 Dec 2025 00:16:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Dec 2025 00:17:19 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 16 Dec 2025 00:17:19 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 16 Dec 2025 00:17:28 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 16 Dec 2025 00:17:29 GMT
ENV JAVA_VERSION=26-ea+28
# Tue, 16 Dec 2025 00:17:31 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/28/GPL/openjdk-26-ea+28_windows-x64_bin.zip
# Tue, 16 Dec 2025 00:17:32 GMT
ENV JAVA_SHA256=1043a56a8e09613f76543d6e9290ff5c53e9cc2bcf0053550a36ad993843bf2c
# Tue, 16 Dec 2025 00:19:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 16 Dec 2025 00:19:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0164f5f587ba9e1d772302470d6e2a40b4db6de9f934fa05a050561fea3c6b`  
		Last Modified: Tue, 16 Dec 2025 00:32:11 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633f413298b2e15783de0dc340c9b8e1057b64d330bca33fab54f4a4f01bd1d3`  
		Last Modified: Tue, 16 Dec 2025 00:32:12 GMT  
		Size: 502.5 KB (502461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b8d8aaf15387684f2422021367394634513c8fbbcfd6572115f3312ea7cbcf`  
		Last Modified: Tue, 16 Dec 2025 00:32:11 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6721e2a2e399f5f0bf873896049e93dfac1dc0022a6acee0a772f927b74bc846`  
		Last Modified: Tue, 16 Dec 2025 00:32:12 GMT  
		Size: 346.9 KB (346915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca57404cf8572be7ed887b827c077822a5ebce9ce65662a2b496f3880628f4a3`  
		Last Modified: Tue, 16 Dec 2025 00:32:12 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8edbbdfa69d7626c275be4163e44bbd10b2efe5e72d102aabdacb97d7a70af44`  
		Last Modified: Tue, 16 Dec 2025 00:32:11 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d696c6e66f21ce3e4d558d98e1c9241243ae96ff18a2731a0ca9be8096d41b`  
		Last Modified: Tue, 16 Dec 2025 00:32:12 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e73aedb3f184b67dd44a6688d0fb685bd8ded0d73c956fd0a4b0061510219954`  
		Last Modified: Tue, 16 Dec 2025 00:32:19 GMT  
		Size: 224.2 MB (224220002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0fe3af75bdb2e869e4d973178a330d7123679be81da876c263fbb8991fbb794`  
		Last Modified: Tue, 16 Dec 2025 00:32:12 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
