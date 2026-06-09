## `openjdk:27-ea-25-jdk`

```console
$ docker pull openjdk@sha256:7b46b38b3f408d09d1cc9112e7868f651290cb95917a7e8dce6f466b5268eea8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.32995; amd64
	-	windows version 10.0.20348.5256; amd64

### `openjdk:27-ea-25-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:cdde5fe0382216ca6ee00cef08c30a6c11ec7d23ab4f1315eb44ef3709e02a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 MB (307715364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f329b90e4af8411234198c5ffe0e335c39db4bd1c698abaaca15ee8ae4ac939`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:44:08 GMT
ADD oraclelinux-10-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:08 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 20:05:49 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 09 Jun 2026 20:06:00 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 09 Jun 2026 20:06:00 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2026 20:06:00 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 20:06:00 GMT
ENV JAVA_VERSION=27-ea+25
# Tue, 09 Jun 2026 20:06:00 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='6287dc1b8b810fc6fb0ecf2ff0f15464e7bbd5b44c45008588224072bbfbaa87'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='6f13903699316f8ee6089a0551ef28686b3bae5b195a98cc4051b365819396cb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 09 Jun 2026 20:06:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ded2aa0abafd1e1e93e05338cb1b14916dbeb283d3862aa21e5d8b0164f4cbf3`  
		Last Modified: Tue, 12 May 2026 18:44:20 GMT  
		Size: 43.1 MB (43080582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197949bdd2d7b8ad2f9adf00ef1a428e8091453257a0b269f98d328d53342f9c`  
		Last Modified: Tue, 09 Jun 2026 20:06:23 GMT  
		Size: 37.7 MB (37687554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f48a60e1f9cde7751520ec91e88ed484a5cc204e99ad277d45dc0b85592d13c`  
		Last Modified: Tue, 09 Jun 2026 20:06:27 GMT  
		Size: 226.9 MB (226947228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-25-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:50b389887db6fcfbe46cf1f8dd15a910bf7f7f076545bd5305b308175055da94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62cf5aa9da7e04d17aa031b5a3c93a91cd4563b62b3c9e5ebe4dd23d69b81a7b`

```dockerfile
```

-	Layers:
	-	`sha256:430e97f54fd48d0f28bc96e983f603588b7d6ca9b4f9713f06126a333ee5f79a`  
		Last Modified: Tue, 09 Jun 2026 20:06:22 GMT  
		Size: 2.4 MB (2366462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50ceae8cd093538a1b17b7fb16a15750971d10faa34373d018f2d1b1c704ab54`  
		Last Modified: Tue, 09 Jun 2026 20:06:21 GMT  
		Size: 17.8 KB (17849 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-25-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:66ed22165b7c903e9e6b0db6496b301d6bce4aeda0a6762f69cfbac70c5cb1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304124197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74cf151a321da3b85f05bbbdb132b84887b92c8433b5249f4cb75649590f06b`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:43:55 GMT
ADD oraclelinux-10-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:43:55 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 20:05:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 09 Jun 2026 20:05:42 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 09 Jun 2026 20:05:42 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2026 20:05:42 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 20:05:42 GMT
ENV JAVA_VERSION=27-ea+25
# Tue, 09 Jun 2026 20:05:42 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='6287dc1b8b810fc6fb0ecf2ff0f15464e7bbd5b44c45008588224072bbfbaa87'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='6f13903699316f8ee6089a0551ef28686b3bae5b195a98cc4051b365819396cb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 09 Jun 2026 20:05:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:523b5fcd95921b1880258a8c56e30985e8f3adf21d143bf177907dc76d6a562b`  
		Last Modified: Tue, 12 May 2026 18:44:06 GMT  
		Size: 41.5 MB (41495695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e200c6d841596c0bf04991621458238854b204790e67988da089131e623914`  
		Last Modified: Tue, 09 Jun 2026 20:06:05 GMT  
		Size: 37.7 MB (37695864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13c46f8f2e7177f3b3129c164afeed6c447a3e62cd644d37e9ee853bdaf9f97`  
		Last Modified: Tue, 09 Jun 2026 20:06:09 GMT  
		Size: 224.9 MB (224932638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-25-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:b3b34b9a4a6c593d9ba78a13b9f9fadd052cce8bd0fd44556706ff6619b68351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ed547878ce474c89dcbbfd8194610f1f6032a08a9d8fb1894cf0514e5f1e03`

```dockerfile
```

-	Layers:
	-	`sha256:6fe366ad27d4cc79c5a3eaf1f7df27cecc78eeda1d197ca8b023f054ff147b37`  
		Last Modified: Tue, 09 Jun 2026 20:06:03 GMT  
		Size: 2.4 MB (2365990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b5187e8791e10bfc777a16e0071499094e91c843b94f71c73e8071f0f5ed974`  
		Last Modified: Tue, 09 Jun 2026 20:06:03 GMT  
		Size: 18.1 KB (18063 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-25-jdk` - windows version 10.0.26100.32995; amd64

```console
$ docker pull openjdk@sha256:95778ee06762dbdad9ab0d7d9841b59ff12c6398e8a8c34a948d3b2c7d95301d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2503421109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8df2bbe78e5c406e4c752d08c57d0a0de8a151d97f0f1868bb17ad1b642ad6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Tue, 09 Jun 2026 22:13:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:24:53 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 09 Jun 2026 22:24:53 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 09 Jun 2026 22:24:59 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 09 Jun 2026 22:24:59 GMT
ENV JAVA_VERSION=27-ea+25
# Tue, 09 Jun 2026 22:25:00 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_windows-x64_bin.zip
# Tue, 09 Jun 2026 22:25:01 GMT
ENV JAVA_SHA256=ca4af1429ae7dc73528c0743f3134fe111133e114e23908c3e729538c6e203a3
# Tue, 09 Jun 2026 22:25:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 09 Jun 2026 22:25:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde3f87c92fa7d0ae280c09db445ee43c8fe0d6469fc2c7ef39eccb597a279d6`  
		Last Modified: Tue, 09 Jun 2026 22:15:30 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e1ff36d89cd1ee2d0e44dd6237e4a88dccf1b6babd7716371f9c3703a19ce5`  
		Last Modified: Tue, 09 Jun 2026 22:25:29 GMT  
		Size: 387.5 KB (387459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a2ceffd1734ee5e91a622a39eee555c6eacc10e80fd75e59c5a0a0fefc7f16`  
		Last Modified: Tue, 09 Jun 2026 22:25:29 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70412fb2931200118c0e6dfe8c6df8605ba5d81e6505c5ed5432d7bee645e487`  
		Last Modified: Tue, 09 Jun 2026 22:25:29 GMT  
		Size: 370.5 KB (370509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:192f89933bef71794d11001402304b82f0ffde2afdc9684eeca4cfba8adbcbe6`  
		Last Modified: Tue, 09 Jun 2026 22:25:27 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c3fcabb69313d325c87148c43d468e13c79d6e8342ec54d49eacf861fd6c4b8`  
		Last Modified: Tue, 09 Jun 2026 22:25:27 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e35814dc77511e79732d987fb85105c0cfeb03948a6c10f1ccf00dd2145984`  
		Last Modified: Tue, 09 Jun 2026 22:25:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c2917348d58675ad00273c5d358c3c31fcbb22ef5b930b45a81a4e24343ebd4`  
		Last Modified: Tue, 09 Jun 2026 22:25:43 GMT  
		Size: 223.5 MB (223512368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00179f524605030d444d7b4db0043a1ce48645157b2bf34beaa5dcb5ac6825d4`  
		Last Modified: Tue, 09 Jun 2026 22:25:27 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-25-jdk` - windows version 10.0.20348.5256; amd64

```console
$ docker pull openjdk@sha256:56e1a4e76a1e5b23a3f40d29a04a18c9a3104301087ee2592fa5e2af53665923
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2356428762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936467ccc106080373840878c15f09f0f4c12931b8d05d5487067c7ed86787a7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Tue, 09 Jun 2026 22:09:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:24:32 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 09 Jun 2026 22:24:33 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 09 Jun 2026 22:24:39 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 09 Jun 2026 22:24:40 GMT
ENV JAVA_VERSION=27-ea+25
# Tue, 09 Jun 2026 22:24:41 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_windows-x64_bin.zip
# Tue, 09 Jun 2026 22:24:42 GMT
ENV JAVA_SHA256=ca4af1429ae7dc73528c0743f3134fe111133e114e23908c3e729538c6e203a3
# Tue, 09 Jun 2026 22:25:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 09 Jun 2026 22:25:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97b5912f4efef19e5de09c2f3306e758f70caacff609559c58cb4937c72d664`  
		Last Modified: Tue, 09 Jun 2026 22:12:46 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232e602be96fc808c304b45b668283c622342152b4a9225529bdf4ca73260ea2`  
		Last Modified: Tue, 09 Jun 2026 22:25:18 GMT  
		Size: 484.7 KB (484749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8db7d132ac49842b25f90039f5eaf07908b688b5926d135d17b82bc34aeddb8`  
		Last Modified: Tue, 09 Jun 2026 22:25:18 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b8d96c980220ea6bb0de529a8ab1bd892a07583f74d80319b6bb38619022a6c`  
		Last Modified: Tue, 09 Jun 2026 22:25:18 GMT  
		Size: 333.9 KB (333920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f15b9240f11d989a062e65a05af41e831601d9be085a733545a871166771886`  
		Last Modified: Tue, 09 Jun 2026 22:25:16 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92fc293dda8de397e529d23ccdd25fc2f108e51b0b6ccf56472abe48e9bb4fa1`  
		Last Modified: Tue, 09 Jun 2026 22:25:16 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe63628f98405d1f810fb1bd1aca538c25e72b7bd4f06386f420490dd8bc4040`  
		Last Modified: Tue, 09 Jun 2026 22:25:16 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81693a552f47388a85fd9ac79d1321af600b1b864df187c9dcd26e3514cd2848`  
		Last Modified: Tue, 09 Jun 2026 22:25:31 GMT  
		Size: 223.5 MB (223476763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980ab414740bb96f1283534d826e58d5b0ffaa32ab637961902c014417adfb5b`  
		Last Modified: Tue, 09 Jun 2026 22:25:16 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
