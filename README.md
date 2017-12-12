# Cuboid-Fitting-RanSAC
RanSaC based cuboid fitting heuristic

Run:
  Use runme.m to execute the program.

  Two 3D point-clouds are included:       
    /3D Point Data/Box.mat
    /3D Point Data/Box_other.mat
    
  In runme.m these point-clouds are used as examples.
  
  In runme.m Load your 3D data in this format:
    points3D = [X, Y, Z]
    where,
    X - x-coordiantes of point data, column vector
    Y - y-coordiantes of point data, column vector
    Z - z-coordiantes of point data, column vector
    
Main Function:    
[model, CuboidParameters, inlierIndices, outlierIndices] = CuboidRANSAC( points3D )
CuboidRANSAC - Computes the best fitting cuboid on the 3D points using RANSAC. 
 If 90 percent points are in the consensus set or 300 iterations are
 reached, the code terminates and the current best is returned.

 Inputs: 
    points3D - nx3 Matric containing the 3D points placed in rows.
               points3D = [X, Y, Z]

 Outputs:
    model - 8x3 Matric containing the corners of the best-fit cuboid
    CuboidParameters - 9x1 Matric containing the parameters of the best-fit.
                Namely, centre, scale and orientation.
                [centre_x centre_y centre_z length width height roll pitch yaw]
    inlierIndicies - Linear indices of inlier points within the input point cloud,
                returned as a column vector.
    outlierIndices - Linear indices of outlier points within the input point cloud,
                returned as a column vector.
    
    
  
