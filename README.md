opacity React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Input } from "@/components/ui/input";
import { Label } from "@/components/ui/label";
import { motion } from "framer-motion";

export default function SchoolAppUI() {
  return (
    <div className="min-h-screen bg-gradient-to-b from-blue-900 to-black text-white flex flex-col items-center justify-center p-6">
      {/* Login Screen */}
      <motion.div
        className="w-full max-w-md"
        initial={{ opacity: 0, y: -20 }}
        animate={{ opacity: 1, y: 0 }}
      >
        <Card className="p-6 bg-gray-900 rounded-2xl shadow-lg">
          <h2 className="text-2xl font-bold text-center mb-4">Principal Login</h2>
          <div className="mb-4">
            <Label>Email</Label>
            <Input type="email" placeholder="acharyaprabhatbaliya@gmail.com" className="mt-1" />
          </div>
          <div className="mb-4">
            <Label>Password</Label>
            <Input type="password" placeholder="1234567" className="mt-1" />
          </div>
          <Button className="w-full mt-4 bg-blue-600 hover:bg-blue-500">Login</Button>
        </Card>
      </motion.div>

      {/* Dashboard Button */}
      <motion.div
        className="grid grid-cols-2 gap-4 mt-10 max-w-md"
        initial={{ opacity: 0, y: 20 }}
        animate={{ opacity: 1, y: 0 }}
      >
        {[
          "Student Management",
          "Teacher Management",
          "Attendance System",
          "Result Sheet",
          "Fee Management",
          "Announcements",
        ].map((item, index) => (
          <Card key={index} className="p-4 bg-gray-800 rounded-xl text-center cursor-pointer hover:bg-blue-700">
            {item}
          </Card>
        ))}
      </motion.div>
    </div>
  );
}
  <motion.div
    className="grid grid-cols-2 gap-4 mt-10 max-w-md"
    initial={{ opacity: 0, y: 20 }}
    animate={{ opacity: 1, y: 0 }}
  >
    {[
      "Student Management",
      "Teacher Management",
      "Attendance System",
      "Result Sheet",
      "Fee Management",
      "Announcements",
    ].map((item, index) => (
      <Card key={index} className="p-4 bg-gray-800 rounded-xl text-center cursor-pointer hover:bg-blue-700">
        {item}
      </Card>
    ))}
  </motion.div>
</div>
